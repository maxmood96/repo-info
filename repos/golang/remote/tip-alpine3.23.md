## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:97bb206b7c74d47809e953083083d6e1e04fe0cf7b8428be6e318232f559bae7
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

### `golang:tip-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:0d238c38bb637c8a2c5aaff6a5ac695c8d160e82cad56df8ca4388753f81ccb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97620084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278a7cd201c1efd3d3850ec0941bdda41774955071da7264e7dcfad8c3b5b807`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:47:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:48:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:48:59 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:48:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:48:59 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:49:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:49:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffdd1b56e12131a6a6bd75f80977980961703f666226946773d2332dcf350ea`  
		Last Modified: Tue, 10 Feb 2026 21:49:16 GMT  
		Size: 296.1 KB (296087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac0d50002cbee1e950896b157d609a44688d9a2715460c4e3c92d9a126868`  
		Last Modified: Mon, 09 Feb 2026 20:03:44 GMT  
		Size: 93.5 MB (93462017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31d9cd6ff483609ec6963b4b5d9a038c6e28ff8624be55f72e5b21bda69a50b`  
		Last Modified: Tue, 10 Feb 2026 21:49:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:15aca406469c79f8a4e7f3243d3d3d1a74bee1da30083064045c355b866edc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdf9ac0c5a8b851cd88177b3ef03ebc9983daa7b04bb1eb22edb7f9d9b33d06`

```dockerfile
```

-	Layers:
	-	`sha256:eb19e622e0e4e292b6bca47f58485b69a745fef98f1952818576132f5e7d92cd`  
		Last Modified: Tue, 10 Feb 2026 21:49:16 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a746f39b71333b333c9f3645d36b12f5c5c92fc39c9f47253809c60d44f191c`  
		Last Modified: Tue, 10 Feb 2026 21:49:16 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:6cc6632d6ec19601f47a734e625a67715154f9295e5bb82a849c12bd86e1da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93718470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca54725fe3d6b51c851295d846c27ba5c2e586ad4509506e4ca19a7e31bfa7b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:45:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:47:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:47:52 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:47:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:47:52 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:47:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:47:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80aa52d386a6f69b0632f2f344e5269ca7060b137646f05246ef96b0664e837`  
		Last Modified: Tue, 10 Feb 2026 21:48:06 GMT  
		Size: 297.3 KB (297260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6550e9c000ea8b3f9a2561021188c21d75815b2a08b1c46ce9ef5f7806416b1`  
		Last Modified: Mon, 09 Feb 2026 19:59:57 GMT  
		Size: 89.9 MB (89851231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c01ef12b3a4c92fa06794b14b3d4840910a39e0fd6f96b9c436166f586373e`  
		Last Modified: Tue, 10 Feb 2026 21:48:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:4cf04eb6d518a4d74281ada7da126a8d359d824d47053ac65db5dee0f72240a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89acf002cde6b27d6f58cd60c36f25d5055b3829d8d1e1ab4322203dcb1d35bd`

```dockerfile
```

-	Layers:
	-	`sha256:84fbeedd4fe047996e7e60c140722f928e05a401592813e323e9c75362612794`  
		Last Modified: Tue, 10 Feb 2026 21:48:06 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:7a786f4c558f3f1291811e997dad03fe93ebbcde2d31308e837953c721323de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93161752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fcd6843e408c3b245894d2443b05d2e628d426d74f4c82e3c3abfd29d32825`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:47:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:50:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:50:14 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:50:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:50:14 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:50:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:50:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95df81cd5de74ea6d8eb712b01e1af6314afe6c4ef1d642c9fdcc6f0f7a7ac53`  
		Last Modified: Tue, 10 Feb 2026 21:50:32 GMT  
		Size: 296.2 KB (296201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60c394ecd04fc3ba572f8a2c09a22e7e8c913f51a7766b230d8afa0ed0ae01`  
		Last Modified: Mon, 09 Feb 2026 19:59:07 GMT  
		Size: 89.6 MB (89583671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7a60f079a15bb0cce3270ac641236a6ffd6103abf9dd4fcb3653b3393e24f9`  
		Last Modified: Tue, 10 Feb 2026 21:50:31 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:ff0d59d8290e31f66229dce6d38c3fc5cb4db22e751251737d8f4f41ee664c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c924b96a017b44b6134b1ea358aefb3231b85a49945a8e8a35f33054893bc9`

```dockerfile
```

-	Layers:
	-	`sha256:5fa6fe23554018a4a3ada08e511ff1abe38939666e4bd5ca09ad7af091b79dde`  
		Last Modified: Tue, 10 Feb 2026 21:50:32 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d70be0542fd7510b238eae844e031fb67ef0ff58d947c98571b9b9bd237ee516`  
		Last Modified: Tue, 10 Feb 2026 21:50:31 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3b14c758b54783c8ef79222b76ae01224749dbad8be16e16c2c3a6e3728332ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92970210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d68b08185abbee59bbaf0a824b7570ee9f0f7a51dbb5f6d8072a9b00a91109`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:46:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:48:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:48:17 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:48:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:48:17 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:48:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:48:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8b2e27fd6052a8ccd86beac770bd94f35ed66c290c86f5cbe50cefee3fc8c`  
		Last Modified: Tue, 10 Feb 2026 21:48:34 GMT  
		Size: 298.8 KB (298840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ae6b9569c22fdb680312e3253454dffff750989d3faaa4cebeb6c55de9593`  
		Last Modified: Mon, 09 Feb 2026 20:03:10 GMT  
		Size: 88.5 MB (88474120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186820bacaf04097ba7fcd9d405949c9ad6bdc76bf2ae8fb9a1633f8ef24076`  
		Last Modified: Tue, 10 Feb 2026 21:48:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:616815fcb7aac5186ba3d38cdb06814b689020dfe7f70bb0d4a87e6cad013358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524d09015b845e7d16a38a99682331313c5f73241c7137503ad57dfa59268122`

```dockerfile
```

-	Layers:
	-	`sha256:9bdba031b82ce8d2dca2552a32ae997ff58fd04a9ce9082c139f2ff020cae890`  
		Last Modified: Tue, 10 Feb 2026 21:48:34 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77d18ac0c4614b6696e48745eff144b9d7c357abc127d92e5796424a0d5840c`  
		Last Modified: Tue, 10 Feb 2026 21:48:34 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:a534f798f8bb6f77ec5fe618d3fe38c2e563d29aa95be4afb9ed5c6ef6b3bbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95503071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57b32e5e2511e74319aa5355dca287e29b50a9c15e1f76cd347eb5c951c457`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 21:47:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 10 Feb 2026 21:49:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:49:38 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:49:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:49:38 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:49:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:49:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b54715d4355d0854107f6fb2fcbe8916c70fb8069c4dab0a45046b59157a7`  
		Last Modified: Tue, 10 Feb 2026 21:49:54 GMT  
		Size: 296.7 KB (296666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9eeab623b500684be7941586d4f5950cd5be2f0139f940b2104a8b3b5d40cc`  
		Last Modified: Mon, 09 Feb 2026 19:58:40 GMT  
		Size: 91.5 MB (91519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9fe3148dc1451fc412cc6983db99f47328ec8625e4d30678d0a25614f80c54`  
		Last Modified: Tue, 10 Feb 2026 21:49:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:5c86e7d61f170199f9007f1a2ad724c873c609caf29f10f81dcd28a82ca1eaf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5b221e1f70bc01fb39a5344a2212348759ef4eb6188683508c4af9ccf919e0`

```dockerfile
```

-	Layers:
	-	`sha256:97932e32ba7fc7a99d8c91be5091a83bd568b907ffd1777c198c7ff9ba4484e8`  
		Last Modified: Tue, 10 Feb 2026 21:49:54 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac1749acc51c206bcd9be4061fee26c37b66afeb7facc5989783664d97c65ef3`  
		Last Modified: Tue, 10 Feb 2026 21:49:54 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:3edb60ffee598b2804309ada0446bb4c2718b4a36ca064f6e292d0b43b803d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94235807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8296bb08b747239dce7e81c545ee04bedfa00e9d78b334b913b06182125c5c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:26:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:26:29 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:32:49 GMT
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
	-	`sha256:e3f34b281626db46d13e5a751b54221f74b1d0be2bfad3701f6dc696782f8809`  
		Last Modified: Mon, 09 Feb 2026 20:28:07 GMT  
		Size: 90.1 MB (90106742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f548714377fa99256875d446830994ae9f45eca7d78ce095c40e90b6fbae81`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:764f133c733a59766356e032afc94001ddb9264cf4a1132932e529b87242f16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5ecd7e6292519d3835391ee4c6cdaed6d2e8a60f02be0f811defa7231dc75c`

```dockerfile
```

-	Layers:
	-	`sha256:1fd60cfb5c4577cd209e2796f0c5fba5881b6dbb66cc1fd612eebc5b9d75846f`  
		Last Modified: Tue, 10 Feb 2026 21:54:07 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27dd812fd6175100f56d7ae654feabcaaf3641af417dde1bf9497e4ef540d36b`  
		Last Modified: Tue, 10 Feb 2026 21:54:07 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:9608ee03911757e67412ed595854d5f7d6b1a48c6ca79aea4ded118fc7f5c9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94523381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b54692188467d72c553dd1d3ae3eb2f66b78c41add03f731f0ff3229cddb11`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:36:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:36:19 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:36:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:36:19 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 21:22:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 21:22:51 GMT
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
	-	`sha256:a23894c629a08e6202ce12c965a7b27818d87e5582941a612a4ef5200db7436f`  
		Last Modified: Mon, 09 Feb 2026 20:43:36 GMT  
		Size: 90.6 MB (90641431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b909a1694bdf03388c102bfee60b9af6a50ae148c4cbf83807e344373acca8`  
		Last Modified: Mon, 09 Feb 2026 21:24:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:b09a688dfc0607863f4c7b8b9e77d9099c7f53b01cb7c29c549b8bab2a31b992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a549029b46d3d8b4e11217a8fcc993b61556e9f1edb3d5de3c3d01b323c984`

```dockerfile
```

-	Layers:
	-	`sha256:8f78d03a75c829190532191b070a9f0a14f6a7ea218d11d3058b8203e991bf80`  
		Last Modified: Tue, 10 Feb 2026 23:10:49 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850ebe197b29fdde63963ca4a0506f125d1b4e1124ef12b3f1544896fd385533`  
		Last Modified: Tue, 10 Feb 2026 23:10:49 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:42f80a90ec74032cad37b5f7e3c8d88cec039aa685248dad38a167f85b3fdcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96671555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635309e194db06dd2c536cef42a0cb6610621a02bf6c6ea7480aa393cc4f351f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:00:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:00:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:00:01 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:00:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:00:01 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:00:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:00:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96012aea906c12635dfd37f261776f274a7fa57e016424f483ebb57edcd7c898`  
		Last Modified: Mon, 09 Feb 2026 20:00:44 GMT  
		Size: 297.2 KB (297174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9ec9ce8a3837e5750bcd10b11df694113758518fac79cbd3aa70f831f2db7`  
		Last Modified: Mon, 09 Feb 2026 20:00:45 GMT  
		Size: 92.6 MB (92648889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928a20c4af2ceae9d1654a1c94327de80dd1489c96dfca1c082be24d1961164e`  
		Last Modified: Mon, 09 Feb 2026 20:00:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:f8fb9bd8a53f837afea4fb5fc4edbc852b9a81ea76ae280abb037edefa57cd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b190ed80ee4592228eb8c7026f5067a17ef8c0fb3eebb033b7290ef5269e89d8`

```dockerfile
```

-	Layers:
	-	`sha256:6449cd7f34a0e30ea27494081d201b5fafb3ac979093d05a4251eed4440c965b`  
		Last Modified: Tue, 10 Feb 2026 21:50:05 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c9f3ef6b755caf9292b82129dcb1b00c516b11e57e771ecf7dd22e8bb8c7f5`  
		Last Modified: Tue, 10 Feb 2026 21:50:05 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json
