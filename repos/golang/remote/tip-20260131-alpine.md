## `golang:tip-20260131-alpine`

```console
$ docker pull golang@sha256:79626fd3216780c9b3b80fc773016dd9f9ee7a183693c95bc068f571943d4ac0
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

### `golang:tip-20260131-alpine` - linux; amd64

```console
$ docker pull golang@sha256:ccb2cd8990e3654d990ded49217c2f9f926ef22e8180798c4d0f51cbfff1d8a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97491471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2428a2be4dc04bb3bbc1cc9278a2d516846a378721a1d11eef0d6ff3946f154c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:09:21 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:21 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:21 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068acc685b6fd14a33202f4971f8bcf09ae0dfcc3c410d1ba1294c15cc2fe0f6`  
		Last Modified: Wed, 04 Feb 2026 17:09:38 GMT  
		Size: 296.1 KB (296083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca55bbd490d4f215c5420355c680b71279036da5d7c91d2d678e32c231a9c9`  
		Last Modified: Mon, 02 Feb 2026 19:30:41 GMT  
		Size: 93.3 MB (93333409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc715818892651794fdd6223f7b454d2d5bd467f00808211e471843ac2a1d00`  
		Last Modified: Wed, 04 Feb 2026 17:09:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a70bd96822dabc3ce6dcab4f20f9eb3dd047b7cc5663aeb210af4cfb029d5589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526672be6593371ffc2fc0b3314b53d31cee43ba6261f0961f0d2d9db522cb1a`

```dockerfile
```

-	Layers:
	-	`sha256:5d12cfdf1b3a61fca2c283b1eed404138cea55e8cbcaf61b7ea2557e82598312`  
		Last Modified: Wed, 04 Feb 2026 17:09:37 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d65089f21e5653182465d3f209447940cdbb8d96e6475b97c6c56176951e2a`  
		Last Modified: Wed, 04 Feb 2026 17:09:37 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:3b7d56235dc1b57990f19b679beafd6a2558abd58e30c040101fd05018439eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93623074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba3ba9ee315cdc9e45d6d7b1c6010a5959de5f2b118e99d27afa0b8897f43a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:10:01 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:10:01 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:10:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:10:01 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:10:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:10:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77c3e893b3346a554b636e8fd2cc2f84f01406c8beec506c6b42f0919b91b9`  
		Last Modified: Wed, 04 Feb 2026 17:10:15 GMT  
		Size: 297.3 KB (297255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0df2db5a6de63ae56b2b7ac54a7918fd9414ba7652c1dadac1bfb31d63c9e`  
		Last Modified: Mon, 02 Feb 2026 19:28:08 GMT  
		Size: 89.8 MB (89755840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc93bd44572efee558bfb929b661f75447ac832afd300eb164b00df0bd074e21`  
		Last Modified: Wed, 04 Feb 2026 17:10:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:35afd936aa5ec1ebfc235fc08f415ac8b7d1ac1a28f8fe93085015736aae99f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8063afabb36e622115062dab0affae3071b5d4012a7fd5eb241794a1383dd731`

```dockerfile
```

-	Layers:
	-	`sha256:3ea015dedeb664bcecc7e54e4fb331c6e779d5c8fd409a41803d16d947542ece`  
		Last Modified: Wed, 04 Feb 2026 17:10:15 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:7406881488b334e09a3b4432d607824cebf3455c84cba8f2411ae1a99c44b350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93054508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e884ee152f8798e4979d73be814452724c3c3ecf906a8b79216acebd225b4a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:09:59 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:59 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:59 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:10:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:10:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c0d5ac447b5421707bb9d236982f3dfe7b22781e68df1be22cf4cdd837961e`  
		Last Modified: Wed, 04 Feb 2026 17:10:17 GMT  
		Size: 296.2 KB (296199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c4d8d165092e2ffa5f6928ecd151df0b8f3dc1362c8f59dcd6d9b09df5017`  
		Last Modified: Mon, 02 Feb 2026 19:30:25 GMT  
		Size: 89.5 MB (89476429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79994454f51754f4768f84771de79f2cfc5023676bf0ef91c46d511220438685`  
		Last Modified: Wed, 04 Feb 2026 17:10:16 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:985b5e2e00ef0b4e9856fab453c100051843b3fbb615e7704dbd830582d167b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ddbcc0972ad96a2b7ee3af11eab9d1c986c56591058c9591c1ece56b93af1e`

```dockerfile
```

-	Layers:
	-	`sha256:0ea4c7ebab8914735b0047d01a9f1727e073d11c57c3c98ce3dfe617bf29b34a`  
		Last Modified: Wed, 04 Feb 2026 17:10:17 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e73c642db2c2e280d95d823e88f7aa649b03aae662f1f0c0c1047cf8395655`  
		Last Modified: Wed, 04 Feb 2026 17:10:17 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:79bd0e21599b02ad7827a41f53f3ce9f2393c6c34ad51f16d3423a027f9d8bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92871793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768caba22a84b95d4086aac928d2fb0f60e3a08542fc353fbe43d493e3fbd1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:08:59 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:08:59 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:08:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:08:59 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1344dc27eaf2b45883882ee3567ffdf92a61ef6173514a01f1beddb66125423`  
		Last Modified: Wed, 04 Feb 2026 17:09:16 GMT  
		Size: 298.8 KB (298844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a2a8a6cfc628c3f67b49421d89d0e853e9d214495c3cea23b3d909be150cb`  
		Last Modified: Mon, 02 Feb 2026 19:26:36 GMT  
		Size: 88.4 MB (88375700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417f84a6c631c7fb27b1aacd477f849c4682a39b96a211639556eefe20a5a8ef`  
		Last Modified: Wed, 04 Feb 2026 17:09:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b1f8c732c2d3e84016219f189993f0c9038c309f8f23505bbac0fe2024057827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bc63a0ff10f62a448cd7280cc975d5f067bd3fe0a69eee9487882a4531b512`

```dockerfile
```

-	Layers:
	-	`sha256:d44bcc3b909ed0ccb82f9136fea37db0d71d924e2b961b6d7c635fdd260bdaec`  
		Last Modified: Wed, 04 Feb 2026 17:09:16 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f223ac7b09423502a369d3a89dc8592527716ce7cc14214bb8d964fa32b77aa9`  
		Last Modified: Wed, 04 Feb 2026 17:09:16 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; 386

```console
$ docker pull golang@sha256:905c6eff2e5d908711355f8de8a2023dfba62509e30bf928f35dee543fa5c67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95390059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d681fdb1da3f7afc9fd1d405fd02b4817bb3fbf4a69b83397fb9259c772020f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:09:13 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:13 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:13 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78954d762815adb4fa44a36124200332bd8ab5d36726c4c90afc458300628f1b`  
		Last Modified: Wed, 04 Feb 2026 17:09:28 GMT  
		Size: 296.7 KB (296667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4604cae1ff047094cf665f2719aaf0543d71e670a699786143900320f6ba300`  
		Last Modified: Mon, 02 Feb 2026 19:27:18 GMT  
		Size: 91.4 MB (91406236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f4cb1361e811c2fde5cf3a2e557dedc6104e07490c349f6c3ab5afd23a1c36`  
		Last Modified: Wed, 04 Feb 2026 17:09:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1121e8d8f56709427be9006386c90621425dcaa3ca5a4e0a18e9f8bb58fcc60f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16329d8faec05c28e0390b58e5f1beaf4f46562d8324574e72fffcd11a70be38`

```dockerfile
```

-	Layers:
	-	`sha256:b5bc3cd37e1ef4dba4a0e50148066291925b384ffe36600b9551dc3bbbcae78c`  
		Last Modified: Wed, 04 Feb 2026 17:09:28 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b86ade65ca012fbe487de74f41981c6d920decc31d7ce80fa378080c13c9de3`  
		Last Modified: Wed, 04 Feb 2026 17:09:29 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:3b9382ff852bc913fe8868e2958369ca4e52230f23e4dbf78ef78f479f669d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94136426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33afc20d1a4e387489ab411ad09c18c2168a6a9a8c128b27488b4b52b8b30d92`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:05:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:32:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:32:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd73d3916f2fedeed1c534628f9a66641a5e1350de62984f598c99fe3383aaf`  
		Last Modified: Wed, 28 Jan 2026 04:06:04 GMT  
		Size: 299.3 KB (299261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e432b6dca22e637a3a25408001c269ffda0f2c5d9306b2f7174d2a31051778`  
		Last Modified: Mon, 02 Feb 2026 19:28:34 GMT  
		Size: 90.0 MB (90007365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7785ae9d9380fa199f7810cdb0026f491fefbdc050bda3f571675bc494177882`  
		Last Modified: Mon, 02 Feb 2026 19:32:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:53699c6cec01fcbabc69a75b9fe9c44a2a81c72ab2eb92e055722c8b7240e333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e690e353cdff54e94fc6199457ca8a96e243b2c61d1a8874d36ece191fd06c03`

```dockerfile
```

-	Layers:
	-	`sha256:539eb8c80f885bac0b3de21b1f9c382c20affdfa13e7d6881af4246289eb6373`  
		Last Modified: Wed, 04 Feb 2026 17:53:45 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d42ffad861cea70e9238d93f6468380904432ced1fc67d47574d55fc541e38`  
		Last Modified: Wed, 04 Feb 2026 17:53:45 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:599a8cdf5e8e0a1f8ebd3e86c5ffd714a8cd2048ffd4d6b88a32a5cbd0623634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94439249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51a2a0c919fdf90c3c6d0365278a9016f6e2ff9a1ff18c1d6f28d77a02a13c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Feb 2026 08:03:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 08:03:08 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 08:03:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 08:03:08 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 08:03:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 08:03:25 GMT
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
	-	`sha256:dc3c8f3022c37addebb7f3bba04877b6aa3acbe5feb276f525d0db506f58caad`  
		Last Modified: Tue, 03 Feb 2026 08:06:29 GMT  
		Size: 90.6 MB (90557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc906b07f89304c50db3daf7c402a93d81433a57a8d9e6c6cf3cf17e83e43249`  
		Last Modified: Tue, 03 Feb 2026 08:06:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:53a827781e309b0cb5d418ed8eba36a80fe91d3f783a6e6d8fb467d63e546383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8289624fc52a58a88451c69054ca366723d42c930471ef002d7742ecf5b36a52`

```dockerfile
```

-	Layers:
	-	`sha256:5cc86a795a0368deeaaeab977d302c3fc316bb272f31f4b746d27527d6cc0825`  
		Last Modified: Tue, 03 Feb 2026 08:06:15 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12e9edebde42a744649e8a9cbb42272ebbfd02270925992c898955bbbc51225`  
		Last Modified: Tue, 03 Feb 2026 08:06:15 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; s390x

```console
$ docker pull golang@sha256:621deadabd01336b8b95615eaa7737c06d000b97939c1afcf273931f738c562a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96593108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c47da78328661ff183a40a5c7b20880d74e2876e2250788fb550f50d612935`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:07:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:29:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:29:01 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:29:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:29:01 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:29:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:29:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b19da3a82072794d62dde7afbbfd822a592c5dfe5b82c058d3ec326c23cca53`  
		Last Modified: Wed, 28 Jan 2026 03:07:58 GMT  
		Size: 297.2 KB (297176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7062bfc50107a913a5fd7c0d090af1366da08b74147cf71ec4490488730775`  
		Last Modified: Mon, 02 Feb 2026 19:29:23 GMT  
		Size: 92.6 MB (92570442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac69d7edf0460e394ef50874b082a893a820797f552ff91067306772b0c1002d`  
		Last Modified: Mon, 02 Feb 2026 19:29:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:def7391aa5c8f2a7a496b46b4e3b8720875f54b96eab333f16eb79b821a96fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46824154ba42a6d373e670972ce9a7fa01323a31079b4f3effcbcf194974b2a7`

```dockerfile
```

-	Layers:
	-	`sha256:01880cb8f86635d1e62a1fc079eec54cb6acef31561eca005a81fec9d96a07b1`  
		Last Modified: Wed, 04 Feb 2026 17:13:03 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239d429036229a7d84e28fb08a2a51544cbbbb976a514732e0f629491770f6a0`  
		Last Modified: Wed, 04 Feb 2026 17:13:03 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
