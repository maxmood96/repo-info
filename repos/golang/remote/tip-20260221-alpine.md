## `golang:tip-20260221-alpine`

```console
$ docker pull golang@sha256:bce34f642d22e69796a79ad5351aec34ec254fda4e9c47aee2c819e9234f07be
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

### `golang:tip-20260221-alpine` - linux; amd64

```console
$ docker pull golang@sha256:80c98b2f591b559298fbf6e35c0b126e8d3e45a6230609a1fadc11eba3574617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97722014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36799d2a361a92df0a95e35ba9c5531a28de0cc77872af928885143462a612a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 18:59:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:00:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:00:52 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:00:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:00:52 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:00:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:00:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aab7fd08c93b92d1bf4ffa9c91cd9f96730a2d31b8beae96be708709fa9bcc`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 296.1 KB (296077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495feeee1b60c984a8277e0860f99ef7f9650e71ef87f6e01f020f04c712c1e`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 93.6 MB (93563958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a3c7431ca94d41cd1559e8378df7ee46baa6b3b5de81a74f0362c0cf39cc77`  
		Last Modified: Tue, 24 Feb 2026 19:01:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:254e606ae22cb7a9cb801655942a8ccd20307e33f23df6de7a829aee93ee871b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf1c571cb949f786b59c60a1e34bce2b7d400293751d40531d3a7111e22377`

```dockerfile
```

-	Layers:
	-	`sha256:01ebe897a0e718a655d77a11ed736d55987c8f9c4151f2860f09c9326d6dbd6e`  
		Last Modified: Tue, 24 Feb 2026 19:01:09 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337b6d89b9463532274627c9757a6f6f3c4d4be499e5763db149ca84abc242aa`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:d1ca2f7adbb55d768d8b743c51cefaaf515ea254e9aeb01dde05ad0c0b76edf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93791665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755ac43348efb03416cfb8e6d1091d9f268077e66b1a43635a12325b5e27a798`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 18:52:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 18:55:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 18:55:11 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 18:55:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 18:55:11 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 18:55:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 18:55:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65468684cd5cedb57d9b6d7eb6dfce87d67815259cfcc4e47e7b1bd90acc3528`  
		Last Modified: Tue, 24 Feb 2026 18:55:25 GMT  
		Size: 297.3 KB (297253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2e155fb43fa9561b40b4cc63456cea59d7ad2c026c1d617fd7ee8b216af790`  
		Last Modified: Tue, 24 Feb 2026 18:55:27 GMT  
		Size: 89.9 MB (89924433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0884bd8cc8cab88ed070b29fe82c67cf5aaa677c8e657cd9f11bf501b199573`  
		Last Modified: Tue, 24 Feb 2026 18:55:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cbf652461dd3fafb791ccbc07b19654d4d4086eccf33eba458c8e858e2e61ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854e66f0937d0b504f278ebd13820b815ad895f1aa47f23584ea3171782ef5a0`

```dockerfile
```

-	Layers:
	-	`sha256:2a0f33b3a7e3838197fe7b47c2b4e37a15941c1558a1ed8f2d00d7ee1459ec94`  
		Last Modified: Tue, 24 Feb 2026 18:55:25 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:ded09a7a9256aefb58e1e4b7f5d8395cd3be9397ccb8a04cc0f9d10aaacdac8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93232565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ffa63676248e2cb2d7d078cc2d2df01cb5303384d036d103fd5db04cf518ad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 20:14:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 20:17:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 20:17:13 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 20:17:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:17:13 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 20:17:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 20:17:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9b3ccc3cd86797ae9f6d32e63153bd207b6c966ae2c73a11e7124d294d1274`  
		Last Modified: Tue, 24 Feb 2026 20:17:30 GMT  
		Size: 296.2 KB (296196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccb983b4dd6150f64bcdff1ff9f7bd363663b337fb9965a8a864ee527592603`  
		Last Modified: Tue, 24 Feb 2026 20:17:32 GMT  
		Size: 89.7 MB (89654487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d175c825a5dc2e216b44612aed065a4708da96aecbb7f0dcaf70dd3649e30456`  
		Last Modified: Tue, 24 Feb 2026 20:17:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6fa89e3752283e66a7b4cc7a24d34571d751779b3af1f997f2ea0e7545d89e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a493b4fd6ceb3c40256fd7cd1f95266c0ec07d51c4a44176e07c1d968a1c2c63`

```dockerfile
```

-	Layers:
	-	`sha256:f6134bda3bf9d6dad3a71ce0b7b3b41016c68e9bb1543169136b7d6d08c39745`  
		Last Modified: Tue, 24 Feb 2026 20:17:30 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e701a01b60d7554868457aa659c77d40e3b31b22b2f82314268b18273c1e5a9`  
		Last Modified: Tue, 24 Feb 2026 20:17:30 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e5e8e59bb6f129048f28f081e26c01502a657967b5701d3a701978e420418f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee8be3a29520cbf9bafacef492ff713f28b54629a9706d44054a8c4c0415b42`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:28:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:29:55 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:29:55 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:29:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:29:55 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:29:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:29:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5498aecd4670288fc9e17a473801304e4726e8320b8f97c3f847f4bd3faa1e0`  
		Last Modified: Tue, 24 Feb 2026 19:30:13 GMT  
		Size: 298.8 KB (298842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991311643d5ba1266ad32d242c21d958ba93238b33b79d32fc0b23bd2b25b23`  
		Last Modified: Tue, 24 Feb 2026 19:30:15 GMT  
		Size: 88.7 MB (88726849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000cf4edba94ee1b2fc6705e1633fabbff67d14fa0ae6ae21966899f0e9ffc3`  
		Last Modified: Tue, 24 Feb 2026 19:30:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:df90ce6081e335bbee75bd1598de735ed78293ecd2a02667d248f0d1aaea6edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d1c580c4179b90f9514e625fbefdd35696322cb1579f93ce27aa00b3ecbc97`

```dockerfile
```

-	Layers:
	-	`sha256:453513c4173c57f63e57a29f41ce2f369af80348fea653d891237f353359ac2e`  
		Last Modified: Tue, 24 Feb 2026 19:30:13 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9222c2ee22b5ccc29a496fb3065a18aec4c2242fa90e076eb63d56a3f54cd361`  
		Last Modified: Tue, 24 Feb 2026 19:30:13 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-alpine` - linux; 386

```console
$ docker pull golang@sha256:a47c43e2128cf79d978829173428edc5e5e290559d1857b4240a6522abbc86b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95438276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809683e1e58dc74cb045ae26414bea06d7bc09aedffa7801a6a813bc5b2a7df4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:25:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:27:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:27:22 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:27:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:27:22 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:27:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:27:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d300469b45744e329c5c2d4a8ab549b996128929bb8ff7beb960cd0efddcde36`  
		Last Modified: Tue, 24 Feb 2026 19:27:38 GMT  
		Size: 296.7 KB (296673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70dcda3c127f8506d59d712159bc64c0b0ee6293dc7af8e7cd42a7bdd642799`  
		Last Modified: Tue, 24 Feb 2026 19:27:40 GMT  
		Size: 91.5 MB (91454447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1caac9d1ce07f26ea28a95018a7525edb4b6885d8c060e0b34a387fb85a81a`  
		Last Modified: Tue, 24 Feb 2026 19:27:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b3a29d1d7df6cfa8214d4fc032fbdcb94c6c18d1b8a3afaf1e32d48cce1cb3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1af08f90ecc2caa4bd9e5e163d1e7c14a787cccb3f7cedbc6513379a69ccdb5`

```dockerfile
```

-	Layers:
	-	`sha256:d8df831ee81132c891ab2298afdeedfa5a24ebf12e380099b64035edfb1c73c2`  
		Last Modified: Tue, 24 Feb 2026 19:27:38 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae1f519fadbd946585ba24941ba6796f9414fefda75aaf1d7316575dafe64e`  
		Last Modified: Tue, 24 Feb 2026 19:27:38 GMT  
		Size: 25.0 KB (25049 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:9e92dc355ed786b1b9eb8d0340a4e2497c94f939537a93a46999e22a3e731b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94376969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a5f97504144277aa03e70dda92e347f876a55d9894995491fb96192d9e35a7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 21:37:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:37:06 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:37:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:37:06 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:37:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:37:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e528c55315b3e5f2f548755f16a234f2386736177558710d4d0c6eaf02151f69`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 299.3 KB (299264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf61cfa0cf71c339b4513ee7439845e2a12d7a655ba1ebeafcd94af8061e69a`  
		Last Modified: Tue, 24 Feb 2026 21:37:48 GMT  
		Size: 90.2 MB (90247905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e737c72bff00ac3d03174c6e41026e6eaa61e164258e0611403b5c43f51b15e`  
		Last Modified: Tue, 24 Feb 2026 21:37:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bb520cc01162652a5c2d381d70d5a2d2f8d82b26d74c1cd5a6ae3f5411349ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b4837b9baf8cb5d4f81751f726623726683ea4e5f36d6aca1da62b2dbb44f4`

```dockerfile
```

-	Layers:
	-	`sha256:d97c6a47a28c9bf4c47fe7abccad7f79f79da4b07b8b48134bc5b6b4456ff780`  
		Last Modified: Tue, 24 Feb 2026 21:37:46 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54875134a50cb26d64d86d5a9a596e6835c17e456e98d480260c40b60f7199fa`  
		Last Modified: Tue, 24 Feb 2026 21:37:46 GMT  
		Size: 25.2 KB (25151 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:b0359915850ee3695cfa55a83f7256cf22b1c601918ffe91d5d24a72c2dba649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94612154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e831cc3b4de8a7b29e039bee06f8058ee261e505fa1671ba0d2e3323d7d7f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:48:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:48:19 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:48:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:48:19 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:48:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:48:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5c9add62f2c1974f9d8b2a5b72c3c47a21eb3a147c7469bf123bb66cc26173`  
		Last Modified: Tue, 24 Feb 2026 19:51:42 GMT  
		Size: 90.7 MB (90730204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357079aecf437f5d3915a4a418edf1e779b208e97afa3f56596b72bdf6c2e5ad`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3260fc697ac4027681d01a5530560fc423a96e223795b73d1c885721f5d66f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2653dc91057ce19aa5d6c51ca35f3dbf64669a97ad3f3b04c1b7accba35a5666`

```dockerfile
```

-	Layers:
	-	`sha256:d2f428d9055872d9c610516d34423b398e663991bc3a2b45acb9a9dbac2e7a4a`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a595c41deccc147200c5e381179bfafe0ff645a4621bb97f6513a00cd40d0e7`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-alpine` - linux; s390x

```console
$ docker pull golang@sha256:4a8269a2f1b0de56386b72fd904ef791c62754c2e7c59fa29d5231f888b2df87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96803133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f1edc09cc7c9fb8f45d1d57c95dfa6dc80856ac9ae576d0dcca2f841d955f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 21:03:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 21:07:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:07:54 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:07:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:07:54 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:08:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:08:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b458f0757ae847edac0ef5c06fa2a870fb3f6c636e4309773936b653ffb825`  
		Last Modified: Tue, 24 Feb 2026 21:08:44 GMT  
		Size: 297.2 KB (297187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8826cd3ddf874113dba9838e707a48966641e8aca63e71ad858398e8db6d0ad`  
		Last Modified: Tue, 24 Feb 2026 21:08:47 GMT  
		Size: 92.8 MB (92780455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975f3e55251af20c55f4a4490aa72d78b43caf0056d1783c8e8d4881767b2d90`  
		Last Modified: Tue, 24 Feb 2026 21:08:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0b6c16f7b2a7e913e946cc6a1ea4ea9a0d11da5a93fcb220f71becc82a7ab4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d442be8ea61cc363408aba7cb981e040b50063562163e22e4aa9129a358abc09`

```dockerfile
```

-	Layers:
	-	`sha256:26f9565664ce5c9699691baaec255a86a3c7d6b29c58ff0fc45679c4a59bdd34`  
		Last Modified: Tue, 24 Feb 2026 21:08:44 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:095aaffa5ac510e2bb3e7d021c79e1a0a00984098377aedaf865be51acef2130`  
		Last Modified: Tue, 24 Feb 2026 21:08:45 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
