## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:bfaca1068fbe92f070ef2ef5ee6da02a91b6055ad972045817dc46529bec330e
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
$ docker pull golang@sha256:7c45ce84238e6abaca80229ed71d0c4293c5e5520c0cdca7f943d66cebce0d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97660150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff2aeaccc49d73b9bf6eaa898594af562db3b771a0a93e0a5b5aa0ae00ffda`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:25:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:25:23 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:25:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:25:23 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:25:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:25:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f95821b67fded1efa50907b80104d7c338cadc4be5e0f9887d77dc687c4421e`  
		Last Modified: Tue, 24 Feb 2026 19:25:40 GMT  
		Size: 291.2 KB (291159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495feeee1b60c984a8277e0860f99ef7f9650e71ef87f6e01f020f04c712c1e`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 93.6 MB (93563958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f28313f4fb905add8a3558a60eb7f8bbd221a866c12e2e1cc460c209726069a`  
		Last Modified: Tue, 24 Feb 2026 19:25:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:bb17c7b76877bc2843a52014953bc17dc2cf858ad910cb9202c27bbdf2b09471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5718423290440f7434072e1ef852cd5e27f509a01893980fc2b029e9ce6e0663`

```dockerfile
```

-	Layers:
	-	`sha256:637e2a3be511babb6d7ff0bb66462c81339188a3b610872d93bd4de3e452d5c6`  
		Last Modified: Tue, 24 Feb 2026 19:25:40 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623a54b63159917d52a97d879de437247f89d7f075cb37763b07ffe1a405403d`  
		Last Modified: Tue, 24 Feb 2026 19:25:40 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:1d5aebb9906fb3b6c7dca40a4d8a6c0970d8e68a41e548f86d00adcf68b311c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93721944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0006bf1bef8ec5630c8b0f3319581112de469e32c26c6edabf1247d7277e975a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 18:53:28 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 18:56:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 18:56:18 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 18:56:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 18:56:18 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 18:56:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 18:56:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f6a7e08c7433ef7f60b7bedc8b5ec41ec20294e0329c824b38aaee4c7f567b`  
		Last Modified: Tue, 24 Feb 2026 18:56:32 GMT  
		Size: 292.3 KB (292306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2e155fb43fa9561b40b4cc63456cea59d7ad2c026c1d617fd7ee8b216af790`  
		Last Modified: Tue, 24 Feb 2026 18:55:27 GMT  
		Size: 89.9 MB (89924433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318aa378df8b9831e7d26f28cdeddc272755d5950fa277cee893585000773036`  
		Last Modified: Tue, 24 Feb 2026 18:56:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e33bacb08549e6e7477eace0a66e7a20eb4114b6b89aa4d0f2cff5579a8c73c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fe02c83be32d1a59f8fff41fd2dce9d0a77ab2febd1f966402e973e4d089f1`

```dockerfile
```

-	Layers:
	-	`sha256:5e09f9d346d500b8f007315f4f45f270fdf3eef13126ba3cfd9ec31d4cca5a15`  
		Last Modified: Tue, 24 Feb 2026 18:56:32 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:b5b62f947c6b46f4b73b0b6d3cf2c4f21c864b0196bf0246b479cbc5a63fde82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93169484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd0cb33753d2f3cc355673bec15584195364cfbc52576ff32af107a8fef93aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 20:15:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 20:18:34 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 20:18:34 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 20:18:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:18:34 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 20:18:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 20:18:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240ce97d3702dac67b310eac3641b191d0f76083580b64ed53633e7b8ca45dd3`  
		Last Modified: Tue, 24 Feb 2026 20:18:52 GMT  
		Size: 291.2 KB (291210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccb983b4dd6150f64bcdff1ff9f7bd363663b337fb9965a8a864ee527592603`  
		Last Modified: Tue, 24 Feb 2026 20:17:32 GMT  
		Size: 89.7 MB (89654487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2289201ab5d81dc14638b352b75dc36d650c63bed19e0d6d878a2a2a3ed79afb`  
		Last Modified: Tue, 24 Feb 2026 20:18:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f5c5e266a006824931cf28fe945ab97275ca42de74fbc3409ac4050ae5445329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba744b2dede32151694af25fe05d46d5f611a26455893586591256a5a84baff3`

```dockerfile
```

-	Layers:
	-	`sha256:d3c32376753cc6dc0a56e0a7ae4ec7506f247501ea7ce503160997629469d3c8`  
		Last Modified: Tue, 24 Feb 2026 20:18:52 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8186ce798d571cacbafcad901139fa9118d69321758f32d85f689781845f12`  
		Last Modified: Tue, 24 Feb 2026 20:18:52 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1d411fb54c7b9a22c01ed0e2621e77a80f071fba7d541d673696d82262fad5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93160627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f4de123df8035cd28267e3ab96e9df2e5de1f2b183f43221605c70cf12bd9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:28:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:30:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:30:44 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:30:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:30:44 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:30:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:30:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad0a773235657abd10a30353af8b0bdb01ea722f2b47af2b86c171be1495169`  
		Last Modified: Tue, 24 Feb 2026 19:31:01 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991311643d5ba1266ad32d242c21d958ba93238b33b79d32fc0b23bd2b25b23`  
		Last Modified: Tue, 24 Feb 2026 19:30:15 GMT  
		Size: 88.7 MB (88726849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab94d3b61e1e6553f2b2324bcc0b93c5306cb0af77306bf61feb57c304ed10ae`  
		Last Modified: Tue, 24 Feb 2026 19:31:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:fda7fa675f3273e265339f1020c00663da8268e93740277bf80ff5d8f01fdc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39256656452eec356780f59953c802f48481f5dfeeaf957cf517019dcff74480`

```dockerfile
```

-	Layers:
	-	`sha256:32b3de27f0d5fa7e284e5fce8610dcd2fec04d30d2941471d935912a00123a4c`  
		Last Modified: Tue, 24 Feb 2026 19:31:01 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4569e0d123cb1602564737c88e9a8acba7bff72e662300579ef9b976ab929c9f`  
		Last Modified: Tue, 24 Feb 2026 19:31:01 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:e70b4e706450caf91295f22abce10b2d9ed5c7254b505105112c18c8d2d5af98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95366954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b349f1d3b04e94546bdb0f1731f5ab78b5ae365da079e4446f133f431e8c2a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:25:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:27:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:27:41 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:27:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:27:41 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:27:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:27:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc8ddc8c775d999d76ce891fe814ab4cfd850ab9fe6e09a1e99a801abab1207`  
		Last Modified: Tue, 24 Feb 2026 19:27:57 GMT  
		Size: 291.6 KB (291618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70dcda3c127f8506d59d712159bc64c0b0ee6293dc7af8e7cd42a7bdd642799`  
		Last Modified: Tue, 24 Feb 2026 19:27:40 GMT  
		Size: 91.5 MB (91454447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3892b86546fb7a9abe3f1ebcc7c6a8c7b6b984a5bb1e848c6bc976ebed2a19`  
		Last Modified: Tue, 24 Feb 2026 19:27:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:93a149fb7e96746c510e9fe2675f6cf97890bda2ff79bc84afc059a572f1db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b626432f261b4726536c4f204da7a5d666f6e25440facde9d285de2a13c36e3`

```dockerfile
```

-	Layers:
	-	`sha256:716cb631043ee2f217acff8f7b5a58b10e6f820f1a7ae56176be1de752fee08a`  
		Last Modified: Tue, 24 Feb 2026 19:27:57 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36702427ae38e83acfa22ff0d6317b95c62ffe5c0f6ce19ed0d5da404b8a4779`  
		Last Modified: Tue, 24 Feb 2026 19:27:57 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:a806a5857373543cf95396a015cb0de71a03159c1155850b322de3962551f3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94238486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c41c845fcaf4bafd5b0e18f5e9501becf2161cc4cc9c24bb54f52edee41dc4c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:40:43 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:40:43 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:40:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:40:43 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:46:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:46:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc2604b78642af0499cb3a1b9f782035bf72390be0d0d2b55d3e7523ce711e9`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 294.6 KB (294647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fde41aed2421b1bfa6ecab656c0c906edcbf89b7187c466f56a4a89af6490b6`  
		Last Modified: Tue, 17 Feb 2026 19:42:01 GMT  
		Size: 90.2 MB (90209384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4af1e46bca926ebb9950d9c408c4e134a54f91931e9e652287e167cdf16e64c`  
		Last Modified: Tue, 17 Feb 2026 19:47:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:10ad538498ff91cd68f81d9cc06a194ff4ed3aa997047c9aefdb14a71879bb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1813e8bc32e0abd2faff7579e9cd91c86eaf682863956ff866423cb0a53c5e5d`

```dockerfile
```

-	Layers:
	-	`sha256:45c68d678d4d06e35474409eac11b7997f8b0e8430614992226e6257f97ce4d2`  
		Last Modified: Tue, 17 Feb 2026 19:47:01 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772a8b0ddf76818ca0b083aa75d61dc4b3cf9f6b358cc91a082e90315e837b19`  
		Last Modified: Tue, 17 Feb 2026 19:47:01 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:f44a43945064931168297ae08b0cf0982b2b49f55df00eacde3118a091ec2656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94539283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3cd63be06cd6a077fbae1b2bbf96d5768f5871a5151869d4227d017a1ab7ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:15:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:48:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:48:19 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:48:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:48:19 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 20:31:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 20:31:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dcab0b270d631ffdfee1c090f676984c71b03f87fc76005b512418b2ec110c`  
		Last Modified: Thu, 29 Jan 2026 19:17:49 GMT  
		Size: 291.5 KB (291499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5c9add62f2c1974f9d8b2a5b72c3c47a21eb3a147c7469bf123bb66cc26173`  
		Last Modified: Tue, 24 Feb 2026 19:51:42 GMT  
		Size: 90.7 MB (90730204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af8c8ae14ec8504d79a2aeb77487c21b453b367885a96c39f3b5b583073ab7c`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7e8999ba28fac140818207a22034efe5324a05f083b35b3e1d5273364e5d991c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9548093b02d94771f26ef28d1e30e82d4510bfb557234248aa3685a083fbaa91`

```dockerfile
```

-	Layers:
	-	`sha256:06b92ac97499145591a7afb2fd7f18bf93f4532412053df625c1c556d07c8b0f`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4605a8ffc603ad0421d6962a5b4fbcf5f4c9b3515aea23b5969596d213b17f`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:73951f30fb35c78796ef9b47f1ea97f95490b635be50b09d1b62155b727979c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96723191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2920ff2e2e88e6bede13b99af9f3e69d8f3510c1b486106791940536c400222b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 21:07:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 21:11:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:11:17 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:11:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:11:17 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:11:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:11:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc400f112129567e6910bdbe94c3d59f4b7f34bdb30c9ba4280d341739a74aa`  
		Last Modified: Tue, 24 Feb 2026 21:11:57 GMT  
		Size: 292.1 KB (292144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8826cd3ddf874113dba9838e707a48966641e8aca63e71ad858398e8db6d0ad`  
		Last Modified: Tue, 24 Feb 2026 21:08:47 GMT  
		Size: 92.8 MB (92780455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0674950d56f42205997fd4d56739d432c75816d3a17ed54661bb3c0a88ea04e9`  
		Last Modified: Tue, 24 Feb 2026 21:11:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0c09fc30cf73f88eecff92d04bc0afbd813d28c69540fa44bd531cc46a3c7405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5f323e898778d46446e55452d7c4818a7b44090d4452b92900794f66dc5c4`

```dockerfile
```

-	Layers:
	-	`sha256:92a8b3f883cea62f39281971fe24fe2dffe5d37c14caa2ea61836b7881b769ae`  
		Last Modified: Tue, 24 Feb 2026 21:11:57 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8f21c9b330638b94b77298bc83ce6664e914e8125bb1a6cd0943b7621efeb7`  
		Last Modified: Tue, 24 Feb 2026 21:11:57 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
