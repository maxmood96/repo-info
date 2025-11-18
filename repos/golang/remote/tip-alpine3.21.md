## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:1f85ce4ca84facc5460db652a338380bb180969c043996701fbb867596b70da3
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:ea44538153281dc194785f442f7610674d85a801286da28895d781157c032ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95898152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee423962132ecd9a14c56dc5b424bf0eebda8113801c13864a0670eeab174c90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 02:40:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Nov 2025 02:41:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 02:41:56 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 02:41:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:41:56 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 02:41:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 02:41:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b24b598dcd2c6246039f8028212b2e1041e5f67f9d1dc096c4ab55d4a7e8c38`  
		Last Modified: Tue, 18 Nov 2025 02:42:18 GMT  
		Size: 291.1 KB (291126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed7b3373fee62cdb53f94efd45c65db5604e6edbc40b8d907723c04dd03d3e5`  
		Last Modified: Tue, 18 Nov 2025 02:42:20 GMT  
		Size: 92.0 MB (91964299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a945660811c27af99cbf47cb0c5926aac4f5ec4fd0a50cea9e4895095a9edc7`  
		Last Modified: Tue, 18 Nov 2025 02:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:547eb905b0b454db22aa3909b4df41706c40710336cbd62e280f851b7acc602a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820bb347bbbece07956caf9a212aa4c82ed12184526aced5640934ab9fdfd8a8`

```dockerfile
```

-	Layers:
	-	`sha256:dd364c29e66a104add6bf2ec7550df8613822349385e2fd90412d4ddfef0ac80`  
		Last Modified: Tue, 18 Nov 2025 03:27:44 GMT  
		Size: 194.2 KB (194205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0d838dd76dfc4923ec16c6268281d7f8203f96d3c6d753dc5a71ab4f055352`  
		Last Modified: Tue, 18 Nov 2025 03:27:45 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:59da64a3c8040642ba8e8cb1d23589464b94910192849ee4b535bfddbbc1b77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92033494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b602e32b7a8fcd121df641c9f96eadfb244c3c635d0940fed5fd3dc2e6a92d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:18:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:17:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:17:37 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:17:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:17:37 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:20:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:20:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7e6a17ab6eca89e864b68e4287488bdf30ac30559934a915b0feb91374d0e1`  
		Last Modified: Mon, 17 Nov 2025 23:20:58 GMT  
		Size: 292.2 KB (292240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c633503e301869c39a50f9afcfc1072f957a321783e002663d5e1707a7e7f16`  
		Last Modified: Mon, 17 Nov 2025 23:18:10 GMT  
		Size: 88.4 MB (88375628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d2c81aaf6738962229b4803cb2088b2b2627d6010290f18b2dc22bf7f5f31`  
		Last Modified: Mon, 17 Nov 2025 23:20:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:29a63fccca3b1a1bbaa7fb0c3f3f2f81347953f8283ef54769e22abeb1c289da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd159486d47d0037436e977fbbb739b21aa6bc9af588d44d2a72b08034a8e216`

```dockerfile
```

-	Layers:
	-	`sha256:9a0f2f1d4ea3e5c717d59db74909bb734035f1f21d59b14d856693a0f302250f`  
		Last Modified: Tue, 18 Nov 2025 00:23:58 GMT  
		Size: 24.4 KB (24361 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:5ff4eb41eca5c4d495164c7f16f8095daf179b8cb6d400040f5b1d365b252e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91502634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fc753e9fcbc099cc0382d13ffabb4bc698d6ba48b687a5975fa639cc50fd5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:21:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:24:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:24:07 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:24:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:24:07 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:24:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:24:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d35a49ddd308c1f5d2dcc75139bff88a0bf6de301a6f671953dfbd60f6a61ab`  
		Last Modified: Mon, 17 Nov 2025 23:24:30 GMT  
		Size: 291.1 KB (291149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a2c69f85dc047cff5b8e0c725d241fb21eed7123e04e156a844669a6e5e5d3`  
		Last Modified: Mon, 17 Nov 2025 23:23:14 GMT  
		Size: 88.1 MB (88112716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8225a378ce62a7976ab0e112fd8c670a18a854f175439aa830e08e39eb4a0b14`  
		Last Modified: Mon, 17 Nov 2025 23:24:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:90b23b386cfb34ddbf1a77e80ecf991c1ec856a4b95d2a25d2e42be427fe029f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c962fe4ba90de4680ad67e68489aec622ec9389fa8cecb849d019fdc67fee8dd`

```dockerfile
```

-	Layers:
	-	`sha256:e569f50466eb119f27f40a1f4dc233d6a95733c797854f078b12172ddaad263e`  
		Last Modified: Tue, 18 Nov 2025 00:24:01 GMT  
		Size: 194.2 KB (194209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be52585f438eb1c62f5efc663ff1f9e5fe295bfb0c653eb61174a226bdb68ac`  
		Last Modified: Tue, 18 Nov 2025 00:24:02 GMT  
		Size: 24.6 KB (24576 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:639e22546dc3988fbbb725d2d95d19da43fe53d4768e2a4270ea96561ae17419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91464308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d5979b39d32bb4e27e9fb4b26ed83fcb66f6ae36d28130a503240fd5d8a12f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:28:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:29:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:29:42 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:29:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:29:42 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:29:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:29:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd25c6bab073d7424a5b6ceaa6404d137311ed8a7d6f620d92498f3d13088a8c`  
		Last Modified: Mon, 17 Nov 2025 23:30:08 GMT  
		Size: 294.1 KB (294059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72859aa41c7126c75b0eaa6f62530c6ab6d97e63fe3d290a8c1d237f80407685`  
		Last Modified: Mon, 17 Nov 2025 23:30:36 GMT  
		Size: 87.2 MB (87177738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bf71629ec91e8ce31312256996b7b695c9bdef7db83f55bab12b9fb1bbcbc7`  
		Last Modified: Mon, 17 Nov 2025 23:30:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:81344b738fd019069a44e850f66a41d7b5b0a0c15abf6f6466bf96bcaf372419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3693c06a22ffd0a68c28e5bfaad510b65b2d9e3adc29d687d94aac1c0e65bb00`

```dockerfile
```

-	Layers:
	-	`sha256:8c2539b47b577fa8ff491669c723c023ffeaa84f6f45c7779aed1b1d23ca3a6e`  
		Last Modified: Tue, 18 Nov 2025 00:24:06 GMT  
		Size: 194.2 KB (194237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a20aaeaeb3ea597a058647ea73d1dd29bd396be3d8713b05cc904b1f22f65e`  
		Last Modified: Tue, 18 Nov 2025 00:24:07 GMT  
		Size: 24.6 KB (24600 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:4db09c10a2cd4ddb682e63930a922dc8151c080500c400903afea0483cd5c48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93661347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe5bfbb0e758776e7b5de0bbca3d20d1129f89ad64dfc890b03e54ca64c1a52`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:22:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:23:59 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:23:59 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:23:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:23:59 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:24:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:24:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4050b87c212e18b617b9564e9cd7e5048aa95251adf7020363adc97892c41aa5`  
		Last Modified: Mon, 17 Nov 2025 23:24:21 GMT  
		Size: 291.6 KB (291589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb363788838918ac7e550b93200cd675ca2501f3ca5b79cee14723fcfb2dfe5`  
		Last Modified: Mon, 17 Nov 2025 23:22:28 GMT  
		Size: 89.9 MB (89904896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b977f9ddbdc68f9a4f020c0d49d5e36be85ee50fa9c3ad3d46e9f2615b6ae`  
		Last Modified: Mon, 17 Nov 2025 23:24:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d9685c8e5fe2d841ac48f41134550ae2a313f86f966aaaac83b559d473d3451f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7319ff64774dfb97d98742e3a27a44bf638344a3e0c23f5bcf54f093a43629a`

```dockerfile
```

-	Layers:
	-	`sha256:0bf2c6d825484d9f5473a20b33c81a28a1f06adfcdf852ab162f0c5013f4247d`  
		Last Modified: Tue, 18 Nov 2025 00:24:11 GMT  
		Size: 194.2 KB (194174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1683b2bf383e7e2070774589973b46793357513880258148d88d2e526b99dd9`  
		Last Modified: Tue, 18 Nov 2025 00:24:12 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:0a1b05c7e429b74342712a668474e179a846206711b8a93987adb588e295f7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92506867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645e573b0cac1d5e1770adf9de85232ab6469471726ce1ca3dff1eabd1c18087`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:53:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:46:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:46:01 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:54:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:54:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0ded502845a7552f2f464d59d34f7ce40a3b171a119e551460f5d03c2e1806`  
		Last Modified: Mon, 17 Nov 2025 23:55:47 GMT  
		Size: 294.5 KB (294529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17fd7fd0e8bf95c13c3a94bedc5db23eb0e60440acf59ef05963d43e52ee79`  
		Last Modified: Mon, 17 Nov 2025 23:48:37 GMT  
		Size: 88.6 MB (88638105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5664dded135b9cea15157795205927023c57ddb9444cbee6a965191f5e735d03`  
		Last Modified: Mon, 17 Nov 2025 23:55:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:86da8fe6f2f83218060b395375a4a0cd6a92604390e41b10a31b244b63829325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412c858b776b59401bd7a03134f7f862df9dd5f7d5fd443ceaac629af2b2d4d4`

```dockerfile
```

-	Layers:
	-	`sha256:982886873c50c291556c72d8c8aff4f04583de1ffb460fe70b5060b51a527d49`  
		Last Modified: Tue, 18 Nov 2025 00:24:16 GMT  
		Size: 192.3 KB (192292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5061afad3bc65fa8f3d67f82ce47f3b65bc3c9793b066e593f8210f540afd407`  
		Last Modified: Tue, 18 Nov 2025 00:24:16 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:8c8c0e3493c9b662aa6f58da871b13808beba01a7990987606077058d57085b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92762825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772044e5703f038020cd0fb5497641c9753f791bf66b8651dc901c1245f508cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 07:48:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 00:22:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:22:22 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 07:48:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 07:48:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f676d248c6000f67f3a138ccf814a525eae5ce7be1aa2856a7ce9c32e68ef13a`  
		Last Modified: Tue, 18 Nov 2025 07:50:12 GMT  
		Size: 291.5 KB (291465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec3a0230c2d0fb9a920af1a0e3505c5c46ba754e2ed64bb7c5b5268656905`  
		Last Modified: Tue, 18 Nov 2025 00:32:26 GMT  
		Size: 89.1 MB (89120201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a328f3d56a67dae2038feb34fbb5ec36f2b710069b4877e4fd176cb931a9f5`  
		Last Modified: Tue, 18 Nov 2025 07:50:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:033dd78151220042f9d3fef2be7e09c2d85d0e7236bf0f3677d16ae94d714fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa034fbb41e4ff6aa35401371d3206373fe09c15ac0707803ea6746087579188`

```dockerfile
```

-	Layers:
	-	`sha256:0cf29b2a18a16be758be749dcd1fae7b155bfd6ca7458e57574b5eb290124a52`  
		Last Modified: Tue, 18 Nov 2025 09:25:39 GMT  
		Size: 192.3 KB (192288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00c130fc3b6789882e906451e5a3f20b40cdd58cdaefeb6f92d4a01570b63fd`  
		Last Modified: Tue, 18 Nov 2025 09:25:40 GMT  
		Size: 24.5 KB (24509 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:4285865b1c1483923e085698d16408ab08876110e56ddcebf1b5bf396911eb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93936599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528f9b516959a7eb1ef4e95b126652cb243a8c770879fca41a7a1d3ac45ad7a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:23:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:26:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:26:27 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:26:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:26:27 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:26:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:26:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a811bd5fbef69ee7cd66f76888a8e13613fc8d7719e032f4c206e093d228ea`  
		Last Modified: Mon, 17 Nov 2025 23:27:03 GMT  
		Size: 292.1 KB (292099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4515f8b1d9cf2143fbca8f466beb9046119009ff0c9973ec41a536bfa5dddca`  
		Last Modified: Mon, 17 Nov 2025 23:27:17 GMT  
		Size: 90.2 MB (90177909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f6bc733cef42e38b2091f95b6b13d1b9b84dc1cf6b6f71d0565b6f89876a6c`  
		Last Modified: Mon, 17 Nov 2025 23:27:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b2ca9285a03018f745d7aa039c983f2b8966233e794973f5f03081e33c55df8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e15bd3e3e5bddce6879155ecf42989133ef4bdb0933a59856749445c061d0cb`

```dockerfile
```

-	Layers:
	-	`sha256:eb3ad7a302f6632cff1fc9f392ccc0dd217429f9da7be535c81221f4133b54ee`  
		Last Modified: Tue, 18 Nov 2025 00:24:20 GMT  
		Size: 192.3 KB (192254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb9372c23604b535a6b5248a6666f69c1429a6c5c01760dd3a2a55a6df0af81`  
		Last Modified: Tue, 18 Nov 2025 00:24:21 GMT  
		Size: 24.3 KB (24292 bytes)  
		MIME: application/vnd.in-toto+json
