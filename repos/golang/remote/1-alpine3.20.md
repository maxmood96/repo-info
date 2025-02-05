## `golang:1-alpine3.20`

```console
$ docker pull golang@sha256:b8d75014b8ecc7b1c7e25984cc092528acd048c09b60f111eee55a28a1535527
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

### `golang:1-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:73e4319e1843e00648789a1cc10802073585d6799c70a39ece7c46a1ec435874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77966657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9452640ca3fae310f357582059dbe38e87355feb9a1200389b67957a6d71a7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5cec81d8735a69060587faecf3f01a97074431dee5b5ff92fa05b7b5439c2`  
		Last Modified: Tue, 04 Feb 2025 19:32:58 GMT  
		Size: 294.4 KB (294384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd968b00abc2f44f5d74b014d2b833a05dd020b5f534f19dca853c409df33466`  
		Last Modified: Tue, 04 Feb 2025 19:32:46 GMT  
		Size: 74.0 MB (74045855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7fa572a88c76277ac45ed59933536275152e95950b44d9ffb0962549f712a6`  
		Last Modified: Tue, 04 Feb 2025 19:33:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:baff9cce8fc742a732444d6e70c39764ecc3bb261b407eee6222f3224fc4fa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea634ac945b846d42a388a5b3f3d3ecbf82a8b05d666f28270c6f876911780f`

```dockerfile
```

-	Layers:
	-	`sha256:5f40899edda4aeedc70093f9c7efc35ae93d94ac27c46871df95d0ab1047a9da`  
		Last Modified: Tue, 04 Feb 2025 19:33:02 GMT  
		Size: 210.0 KB (210037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e06855de05a36f8753e7fa258192a645fad8caa0204b566ace9116d27555799`  
		Last Modified: Tue, 04 Feb 2025 19:33:02 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:5eb6e7e5eadb05d0f1e912e1ce405bc67564ae29939068382fefabef1532cead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75862774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b75b53f189def19a6005087364080a6a4822af7065adb56bb8f2afd18126d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a70656b186536acaa70853744917e9a0b358e5475d451816ac52af6b864bc`  
		Last Modified: Wed, 08 Jan 2025 21:57:17 GMT  
		Size: 295.8 KB (295828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc15bd6dff137475f22b6631116b4ea034384c5e21f31d1ca51949d8498e95`  
		Last Modified: Tue, 04 Feb 2025 19:33:14 GMT  
		Size: 72.2 MB (72195315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737a6416d3add5be58c09a6629434bdf329a75136771da5d43056913d754aab0`  
		Last Modified: Tue, 04 Feb 2025 19:33:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:adf99eed3e72dc8a578c9833044fed07387cc8c2e7817ea68fd16e734f21e9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f83f5da47e7de4fb5b3a76c7ac026395b7dc163e2bb6712afd38af80158c34`

```dockerfile
```

-	Layers:
	-	`sha256:eeb390be4eafe07f73a09c12d71f57d163b2c50055160a26572ac46537519d3a`  
		Last Modified: Tue, 04 Feb 2025 19:33:12 GMT  
		Size: 24.7 KB (24737 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:98f5ddb3ec67a9b7ad161b74b2bc4923795003908834c2dacf6ee4603e4e504a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75584351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4803b54a2a30419f07c47a0edc2dcf3c73b35521ce40d9728a3c1a5ef9559886`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf03070cac649166aa1b87cea610615d91250eff95c905990cea3c1d510e67`  
		Last Modified: Wed, 08 Jan 2025 22:34:16 GMT  
		Size: 294.8 KB (294759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71181da0f46bebe3348744084ada18c7bb3fc1a115b2faa229669f2846f8a617`  
		Last Modified: Thu, 16 Jan 2025 22:10:17 GMT  
		Size: 72.2 MB (72193920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8bc543d95cb030f065e8d4e1924017af15123649eb283dcbaa694ce2ff7596`  
		Last Modified: Thu, 16 Jan 2025 22:12:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:aaada7b3bdf85a5e4fd62fe2392340a64983e65618945d94ec77d6d86a8153e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (234988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c8e43c740d0285f9f5bf2ea36b835454d593db06b9309fa1178a86514be045`

```dockerfile
```

-	Layers:
	-	`sha256:7be78ad7c389a5baa332306ed1fdf6bf134606589b369f8d1acd7c75597dcc5c`  
		Last Modified: Thu, 16 Jan 2025 22:12:08 GMT  
		Size: 210.0 KB (210037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7cb2478a54d21b911a9d7652be9a8d7241a53dc1254502b871bc25cb86e0fe`  
		Last Modified: Thu, 16 Jan 2025 22:12:08 GMT  
		Size: 25.0 KB (24951 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:95a38817cd5dc42bf494d5ebe59dc56a981f0a71706d56b7daed744dd425b56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75064677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f6832c2d2644f502dda876e6faaab3a78c8f6b1ddd80f373dab003972f6a47`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07219bb1974a1749c2d7ad8e3c5020b1a9e55023216926da79ccd2a39b4eef`  
		Last Modified: Wed, 08 Jan 2025 22:40:18 GMT  
		Size: 297.5 KB (297474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d514b7aa85ba6aa1665a90e4a24f9a4312a9ae69f1e26235cf49d08b80c7b`  
		Last Modified: Thu, 16 Jan 2025 22:08:29 GMT  
		Size: 70.7 MB (70676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70e38ab9e143042de2d2c8f11030a42b5de9da41f1c5f2bb6179dd6115237e5`  
		Last Modified: Thu, 16 Jan 2025 22:09:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:f58d880976b9abbaef88782fb4488e1f1c3591bdad46d5b9c2994ea58053516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d92390419cccfd3a9e9f2f78cef466eff2d9497c75d09e5bb4de378c776bcd`

```dockerfile
```

-	Layers:
	-	`sha256:9c5e467da35a1a23d5014df0b1158c82ee03bafe916258cdb01d7cce36b1f8ef`  
		Last Modified: Thu, 16 Jan 2025 22:09:47 GMT  
		Size: 210.1 KB (210093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a811ae7fd0565c81ba05631f986d207d747a4263424c6bb17e0584e1b98a119`  
		Last Modified: Thu, 16 Jan 2025 22:09:47 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:e9fe19b5ca113464a0a78fe5585f73b85392f642e726b9d40f63809381db0f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75686082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86c0a79d9ec9629d62af7bafed24f3bf615654e88a3f3f818ed3e83f0147eb9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad06f3721cbc8cec3028dd269f2bca928b30078bbee45fef1882d7e249cf339`  
		Last Modified: Tue, 04 Feb 2025 19:32:49 GMT  
		Size: 295.1 KB (295140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b77728945927969d0c8ded023b60910b4b7d2a79c658271ebe4948de9a6d578`  
		Last Modified: Tue, 04 Feb 2025 19:32:35 GMT  
		Size: 71.9 MB (71919814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce0ff1218cdae597b4f7e8ceaa0c4d290b9788d13fac438550eb4f10fb467f5`  
		Last Modified: Tue, 04 Feb 2025 19:32:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:15a1bb76dc8adb9e9f257d077b04b1ef83098ed8fbde45ec4d47cea79d6ee886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 KB (234790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1cd881a443e4cb138fecf1e69830556f111c67ca971f5a59d5ddd586d7ad9f`

```dockerfile
```

-	Layers:
	-	`sha256:f4b138b727c3ec240066fe107f67064c2b0acda9c523c1f61ec58a7c89bf16c9`  
		Last Modified: Tue, 04 Feb 2025 19:32:48 GMT  
		Size: 210.0 KB (209976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce74fefc1de695a0b39e407e8e483f8f481573004ad752ca741d8d31e4a17d9`  
		Last Modified: Tue, 04 Feb 2025 19:32:49 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:334dd508e861e65fc844a6e0bbe296220184fc98e92a812c4eef852378000f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74710564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6737acd4958bb5b54166b4417f6eebc50515af19a286cf40acb06c38b5500`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bc8515280eafb56fff5db8a8a3f9b1389a9563753c21ecf558291e30e86e2a`  
		Last Modified: Tue, 04 Feb 2025 22:34:44 GMT  
		Size: 70.8 MB (70838106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cbd0fbb95cd1569eb7fe3cd06d943521c195375a002f52a1c58deeb15a3df9`  
		Last Modified: Tue, 04 Feb 2025 22:36:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:7da4a71d33400d993bf39d230062091c117b321920de7ccfd51d730545752f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 KB (233054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5383019f3cfb1a55c4d9f36ebcc39898da37dbe723d258dd322228989d6624`

```dockerfile
```

-	Layers:
	-	`sha256:bb8be2647d34d8157e662d2d0e99cf0440eb4b909a97211f1688642f295da752`  
		Last Modified: Tue, 04 Feb 2025 22:36:10 GMT  
		Size: 208.2 KB (208156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35ddc89830ce4855b0cef944301b2f1bfbc30890fc0659d085288553c201430b`  
		Last Modified: Tue, 04 Feb 2025 22:36:10 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:cc66fdb84088847afa99c9b86597c53e61041f4e78ec01a1191552396c77ff6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74903932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ca0dabe90269843fd05485d59c45cbc9e1f196e3b42ed9e87bb1099d39b688`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816c3897a63cf7689a7beab4c1f1af77b6f15050c01df55852c40f878936f63b`  
		Last Modified: Fri, 10 Jan 2025 17:00:34 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bcbafcf86e581c838713d6aa93c05a7dd1d0a064c9bb430f1bc2e58c504369`  
		Last Modified: Tue, 04 Feb 2025 19:37:04 GMT  
		Size: 71.2 MB (71236403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48a91ab3130df220b3603ac4e3497efb8af727ffbf26271e2564f354f009f7a`  
		Last Modified: Tue, 04 Feb 2025 19:40:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:93c0f3248217e3f8dad653baa3347b894f27c6ff2c81006e6125123e2b2b974d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 KB (233050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69339590cd236e6cb6b44074ab08097f1c9a2a667f9967e01eef7adbbaab158d`

```dockerfile
```

-	Layers:
	-	`sha256:24920c673c046f8ed5da5734c19f9f0747c24583fbc4ace953d8b41708ed063c`  
		Last Modified: Tue, 04 Feb 2025 19:40:21 GMT  
		Size: 208.2 KB (208152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e51a866b04e77e0e997702f6e2fbf5370765b1261f3f66dd44573f7f9561c50`  
		Last Modified: Tue, 04 Feb 2025 19:40:20 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:deecf15b15a204c7de532bc0f4d83260d91c71c0375b9da0d35808e65ac33ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76713863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04774b96fa4fd598bc40435fc50d25181524f517b61107198b9ead36e40d14a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27beb3ecfc66a05c4717a47324657a7da44cd7a01b554efb4ced3c7c613a567`  
		Last Modified: Wed, 08 Jan 2025 22:26:47 GMT  
		Size: 295.7 KB (295699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b567a3d856120b002d262f7c532f30adaa977477b055fda3e7047c19dfbefeb`  
		Last Modified: Thu, 16 Jan 2025 22:11:06 GMT  
		Size: 73.0 MB (72954684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ad89383bd4ec340d6a2b82b4b5b7c338409021cd87f47871b0af971fa0fa0`  
		Last Modified: Thu, 16 Jan 2025 22:15:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a72d46976a70a645838ec1d057d3304a7bf5c055e7babd980b06622db403796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 KB (232936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95e203e1f8273677572574dbcbb03966d1db8cba790fdea55f172710bf9aab`

```dockerfile
```

-	Layers:
	-	`sha256:8aab1c97a885d33591863695e23b7996226b83851c9137daade25071d3230500`  
		Last Modified: Thu, 16 Jan 2025 22:15:42 GMT  
		Size: 208.1 KB (208086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621008441d3573046a9c629d7eccee5690b8a15f85985b84aadee6fe39c4ad65`  
		Last Modified: Thu, 16 Jan 2025 22:15:42 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json
