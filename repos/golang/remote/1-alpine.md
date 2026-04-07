## `golang:1-alpine`

```console
$ docker pull golang@sha256:c2a1f7b2095d046ae14b286b18413a05bb82c9bca9b25fe7ff5efef0f0826166
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

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:c216c4343b489259302908b67a3c8fa55b283bdc30be729baa38b9953ca28857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71378552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3121f6478954b90816b44bdfb23e005cf29d208f08e2dc101f960a75282c479`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:14:04 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:14:04 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:14:04 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:14:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:14:04 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:14:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:14:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d8f694c0bdd364dd5408954388b3f41362d164547ee1220cf63228070797e`  
		Last Modified: Tue, 07 Apr 2026 21:14:20 GMT  
		Size: 296.1 KB (296072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55da06e3b41084804b2e5dbba71d35d26478b19ba8055d07a393cae22e9935f`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 67.2 MB (67220501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e09229ea5a178f7882e59cd830c6d8179c2c018c6bfb99f585cb87a716c0ad1`  
		Last Modified: Tue, 07 Apr 2026 21:14:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8717705476c556b7e60893077b74c0ab058a81ec38e5d5f2d2a69eba3c8621ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 KB (223050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fccdb4b4bc9a72c8952061bdd384aca399c998b830f9bea22468ab6aa6ecb1`

```dockerfile
```

-	Layers:
	-	`sha256:effb4eb9ed179326ecbeb737f6ee74d0824ce16c73942c27c705086abca7cc7f`  
		Last Modified: Tue, 07 Apr 2026 21:14:20 GMT  
		Size: 197.0 KB (197023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87bbdb8a5de4eb9c4d79a64433a2303c51647118f10164385d74dc390df5e568`  
		Last Modified: Tue, 07 Apr 2026 21:14:20 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:dd094f998c8853e4b7438ee8ad62ceba28c9304c6e49016f446b53665933bd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69618260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4b410a7ac4a1a2a74ddc9dad152c98746870c1f8e340cca3afc824f945f599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:16 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:16 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:16 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e87b3254de769a256e43be6b111c8d3e8808cd67aad52a0b72e430d18305691`  
		Last Modified: Tue, 07 Apr 2026 21:13:30 GMT  
		Size: 297.3 KB (297257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e327e2b14e32d059b1daa22f82c1fb7fa98060bc20d47dd6686da42229cba8b`  
		Last Modified: Tue, 07 Apr 2026 21:13:32 GMT  
		Size: 65.8 MB (65751024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5a4e2604d6b26da5598245b3c1e539bc25abbe79f898b39130896e768b62e4`  
		Last Modified: Tue, 07 Apr 2026 21:13:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:645b3b967fb77c0c9f1ef55c1a17bc43b913689cc7283b3115985334b17fa53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2dfc8353c1af149978355daba45f194ac8ce32975c3e3df70772c1238af16d`

```dockerfile
```

-	Layers:
	-	`sha256:0b00db71707a46c368c5bb393ccea93f09feecc970a80340d9e1c9a823ee6692`  
		Last Modified: Tue, 07 Apr 2026 21:13:30 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:cb948f58dc4a7e5ba0c2b832debe501f241309788791d1e14f3f1ef3a899a1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69329056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9987448f38b01d7d4077b2a4a123f4c7de9a2a25cbb081775276bfc85d181cd2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:14:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:14:12 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:14:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:14:12 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:14:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:14:12 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:14:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:14:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b3d19c8966500e34df8c4d763f6c1a8f37be1de7321cdbcdefb9d01c6a70c`  
		Last Modified: Tue, 07 Apr 2026 21:14:29 GMT  
		Size: 296.2 KB (296196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b788dba2764741459e09a0ea7605019deb67fbed88a9a86398f61f23be05dfc`  
		Last Modified: Tue, 07 Apr 2026 21:14:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:48496cd7334a277362aede1369a0af6c907cda4b7a6d8ad83e412997774b267e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 KB (222590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650c874ca29529a53d9e64fcd99ea2b5e34e31dae2862c643017c5aa03709142`

```dockerfile
```

-	Layers:
	-	`sha256:87d614d37df9006e4fc060a2822de6b0d5d75f8a6310cdb7b5d92e84602e54a9`  
		Last Modified: Tue, 07 Apr 2026 21:14:29 GMT  
		Size: 196.4 KB (196425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f83a999c56672f753037622857c8452655891a10b45c005a319febb6dcd9cb10`  
		Last Modified: Tue, 07 Apr 2026 21:14:29 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6440890bcd2ad73b3d86cafe7902e65c39167ed2e8fb022d478c3014f2d750ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68604852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7e7d5b7ed2d95bec5040fffb7aaef7379c7c71cf02bdd09c78362c5c642f70`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:48 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:48 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:48 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1f5a7ce8cd2196e4ce4b6d177083870b0457fefda71ebf6f3eea195fb8fca1`  
		Last Modified: Tue, 07 Apr 2026 21:14:05 GMT  
		Size: 298.8 KB (298845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e89efc4b5ec39fa30d639b12ad2c7fd994a11ffa608e77427a882d73768d76`  
		Last Modified: Tue, 07 Apr 2026 21:13:44 GMT  
		Size: 64.1 MB (64108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9954570ab45fb86f36b4100a20e81ac2a3738a59e2c42f9de3d1ef5d104f5eec`  
		Last Modified: Tue, 07 Apr 2026 21:14:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:53783e6e7a2304387f6230e861eca307c2b4eae8afe1d81ebc6ce32739c65446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 KB (222686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497970914b0ffa71245ab02e77d586a5efd462fc63f2623a99d9314e4141e9e`

```dockerfile
```

-	Layers:
	-	`sha256:4ef0f1f39d6944fa684e45e27e99598a4a93dab03ff6ae290a671fc94a5063ca`  
		Last Modified: Tue, 07 Apr 2026 21:14:05 GMT  
		Size: 196.5 KB (196477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7febc241fb0ed2a257b01c18270cdc6cd3137f51d14d89a8090f455e802e6520`  
		Last Modified: Tue, 07 Apr 2026 21:14:05 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:a7c435cf7a8f0bb074cb89e1b996cc49c745d61eeef9738cc00eac4c33f482ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69525580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80efd7dd5466781118dea9d4a15ba5407300e6dcd3f8a849f8da6730eb346f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:14:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:14:25 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:14:25 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:14:25 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:14:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:14:25 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:14:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:14:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a56773d9d5bd96ca1adf90f73c06868bc94ce6d5e89a16582e9ef21082b1bf`  
		Last Modified: Tue, 07 Apr 2026 21:14:41 GMT  
		Size: 296.7 KB (296657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469b29d109e367ac43f3e67c104c046d01b1c6cca80443b728b2d38a262b476`  
		Last Modified: Tue, 07 Apr 2026 21:14:00 GMT  
		Size: 65.5 MB (65541767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38b39b4a23cee689dbe37e996c9428d99d13490a5ae0e094b333c0bee1e16a4`  
		Last Modified: Tue, 07 Apr 2026 21:14:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8c143cc763676f595dd103586c3c7a7b180659d0ad009b1435bbb82f71546d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 KB (222933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e2d5bd10b9e80c591858e7084b87e9400da6d9da5f33670cf59534e6450776`

```dockerfile
```

-	Layers:
	-	`sha256:8700bf3c0e059131370e08956ad50657d4693960c9d4211249c636d5be5c3b27`  
		Last Modified: Tue, 07 Apr 2026 21:14:40 GMT  
		Size: 197.0 KB (196962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e317df157518b68e672e05eca52925e8ecbf6a6b6d23b42fd10dc74acef71e`  
		Last Modified: Tue, 07 Apr 2026 21:14:40 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:c83788437de8cefa3b80f90bea66e1aa1d95846b7556a6dc57c53fe9cc23ed8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68886837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac36462cfe31ed6d22bd50fbcd2ad5c173d2f85c8c097053c8127626266288d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:28:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:28:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:28:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157c37b8ca35f88bf66161b72bc1761ade8e543ac3a14868075a68b5dff95e5`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 299.3 KB (299270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59cd64739ee2c1db9b4eb7c08338d6773eef47b2c94a225b64cb228ac665cec`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1b4f524db403d3efb58166e101d88192156003ebd77b92de81e1e632746a039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 KB (222545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2035fff0dfec2a43c4fb6ead818b2158eeaa6cdb96719b21060ea2366d65c845`

```dockerfile
```

-	Layers:
	-	`sha256:e7d73ae4ebaff0cf3d0658d55d26d3a873621067c51943442f2c8e3275465202`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 196.4 KB (196446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a3eeee33100bd9f47a57d74773b2e1c15734d09bf2452cba4841b82a9ba7f6`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:cefa96c59339c74d73f51703a41a24cc3b520a736236bf7a6580df1b2883e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68975814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bb46fbe4d3e2609f55fc4ed147fb2108d70c9bb8ab52fa217b20363b1ee942`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 08:51:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:31:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:31:22 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:31:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a48053074547bb1f8e43c4e508d8a803d45b52e98210c3539d09ceb870090`  
		Last Modified: Tue, 24 Mar 2026 08:53:11 GMT  
		Size: 296.5 KB (296514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18820a12075d850af6085d052799ca6c42481c33ddc318143f5caa48480e4d17`  
		Last Modified: Tue, 07 Apr 2026 21:34:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4c346f825e10059298946e2fc2011feafc007183fa7b2c3f0269d07e78f1f8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 KB (222541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871bdf797d0720526445af2dec7fd4adcc741cc9941d795f8947b167307df50`

```dockerfile
```

-	Layers:
	-	`sha256:4de9839b9b099497236b198e6f2afcfca248cee87330100e021cf732d6d601cd`  
		Last Modified: Tue, 07 Apr 2026 21:34:17 GMT  
		Size: 196.4 KB (196442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66388c961ddc07d76c8debaa85b64b168abbe9790e2387fe6042c4b012ff0e53`  
		Last Modified: Tue, 07 Apr 2026 21:34:17 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:5bf0884a7d4208d1f79c7cf69527d2647e78f63144b2f2a94cc6480ad9fdbaca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70454874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26c0590965f8eb7c558d34921847936d585e7570d3e302395bd426b2596e8b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:11 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09b3320db87c0fbe713adce5ff43836b299964a204ab829de72270c3d2d4c3`  
		Last Modified: Tue, 07 Apr 2026 21:14:59 GMT  
		Size: 297.2 KB (297199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8b98e3267789cad196300f0ede7760a8353c331b3221d7fb9a3a72d8fbfdf`  
		Last Modified: Tue, 07 Apr 2026 21:14:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1a483e8a1682e24e8a24125c6528f52c3da5d9a2af0e251ecd740cd44225f517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 KB (222226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ba0c0579b9f63e14fff1c4f657f7fdc1d03a4295e1a623d899b2dda5683463`

```dockerfile
```

-	Layers:
	-	`sha256:a6d40563399d00a4f44d74ea98f353984bdf6bd8087ff854a0ab05a4a2cae907`  
		Last Modified: Tue, 07 Apr 2026 21:14:59 GMT  
		Size: 196.4 KB (196372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d49f87f8a849ac11a11f4379df38ca187d3909b675f9cd494c843e9843d5c5`  
		Last Modified: Tue, 07 Apr 2026 21:14:57 GMT  
		Size: 25.9 KB (25854 bytes)  
		MIME: application/vnd.in-toto+json
