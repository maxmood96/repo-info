## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:e7b8488e2711f5ee398c738dc4fdff069d53e8dc7178114665943794d9b7c7e2
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
$ docker pull golang@sha256:8b042f8c37e3815e9b2313f98c7b498a7d07aa89401a474b2020e02776f2ea8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99150172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8454ad60c04040fca1fce8042c9655981c3a3be23c57f9ba09a29b5dd347788`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:50:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:52:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:52:02 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:52:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:52:02 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:52:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:52:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98ede4c300f2511cac01f08f403bcd489089f6241b22d052fb65092d4bb5e1f`  
		Last Modified: Tue, 20 Jan 2026 18:52:24 GMT  
		Size: 291.2 KB (291165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6a5b8343289eb0c3c52bf550e1fe8d1945ce754f136a34955c716ac7e17d7`  
		Last Modified: Tue, 20 Jan 2026 18:52:04 GMT  
		Size: 95.1 MB (95056396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a1818165eef239caf62093b60dd93166432f66c1dc79c147ac15773f940926`  
		Last Modified: Tue, 20 Jan 2026 18:52:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ab82310c561dd4b740d99a63340bb2f808d51457ea812a1c1446da02757c680a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebedab649e7321d794eee512934493a86ededaecab464c0f8aa4cd8830477f3`

```dockerfile
```

-	Layers:
	-	`sha256:f69920d13a98cf03dd897ead72b06661607ac679c5003d7956cc061d8a6441ff`  
		Last Modified: Tue, 20 Jan 2026 21:24:36 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d717847126f1c49b57b4ef5a11146c4009b39a2381663b21933b046eb93f87`  
		Last Modified: Tue, 20 Jan 2026 21:24:37 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:8bbb3a3c8e07964f5f735635a6139ada67d842b9232ac098d4e127bfd9f6269b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95202272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50c7a55d3d58571115f7e0cdf3f3263c67e4b56ad43539bf9834781cf1438d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:50:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:52:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:52:57 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:52:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:52:57 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313a00b98a506ceab6bc44da80139841e634d9c683b2cc7bcb802dd1a1f5524`  
		Last Modified: Tue, 20 Jan 2026 18:53:11 GMT  
		Size: 292.3 KB (292311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed3bda5a5c34f85b217d1a214cc216a3a9141352cc733d31928c895ddc9b66d`  
		Last Modified: Tue, 20 Jan 2026 18:53:27 GMT  
		Size: 91.4 MB (91405722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aacdf2917d2dd79ef75a59efbb434fa613e4f93d01761414c0f10c0b714cd12`  
		Last Modified: Tue, 20 Jan 2026 18:53:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:c3a5bd70fc6d37b3b901319bd07e72917eb6d259972dff1f3666f1689e870ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cf3351596256d10eccc7c8009c428556b14711088b22ce76fdfc257a131fd7`

```dockerfile
```

-	Layers:
	-	`sha256:3211237260250b28611cea90f4d849d3bbc4c198c27206327dba0ed416c09a17`  
		Last Modified: Tue, 20 Jan 2026 21:24:40 GMT  
		Size: 24.4 KB (24360 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:339846775ec49ccec22baed47adf3d7a83bf21e10649fcbabacbd881d3848614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94640711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9e820c2787210086d470dcd5f42b1faa5774f99cd202492323468c6162cf0b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:50:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:53:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:53:10 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:53:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:53:10 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab24fdbac5aac24d71c4262299109bf0f40dcaded5d84019bc697dbb555cc6`  
		Last Modified: Tue, 20 Jan 2026 18:53:28 GMT  
		Size: 291.2 KB (291211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbc1ebe88b1983952e0d3b08c79038602b5105dcae7c600fd0a26d7e35cad0`  
		Last Modified: Tue, 20 Jan 2026 18:53:18 GMT  
		Size: 91.1 MB (91127787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa024c71311fe4b15deb41337d4453bfa7779723232098b94ffa454a743512fe`  
		Last Modified: Tue, 20 Jan 2026 18:53:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f23f1a38360d39aecba84de764b85a777513f40bdc912611e58bf71a83f48e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3982ccdaff56a7291655629d54e456ac01d6539fa68ce8b5c0106288ca8b97`

```dockerfile
```

-	Layers:
	-	`sha256:d318afb648ffd15d1dfc7969092fb108987cb836045563c4018783bcce9a1c9d`  
		Last Modified: Tue, 20 Jan 2026 21:24:43 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71e1d6e28ff9787d32afe5d1b9b8ede695cbdbe7a6d58c42e5e0f55294540d6`  
		Last Modified: Tue, 20 Jan 2026 21:24:44 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8a06e013863cd3df506aaa28261b6404f7788caf37c7a6bd5b647531a9e210a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94564303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4697e71a33f47f82be53607ae378086d7b5e91511d6464c728c277f15b50908e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:50:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:51:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:51:48 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:51:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:51:48 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:51:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:51:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95258cae4e50a4a7c408eb5e051a9be233c0a6339e25968d7273cc9b89d57508`  
		Last Modified: Tue, 20 Jan 2026 18:52:12 GMT  
		Size: 294.1 KB (294117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8704a9b461e9f9c3cf81dacaf53a5375b1bb82e9194e9ce88802dc458b5979`  
		Last Modified: Tue, 20 Jan 2026 18:52:00 GMT  
		Size: 90.1 MB (90131959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a621e1b5b8b582fad5718ed8a68e628ce11918a13bb31cc1258f3211965e6a`  
		Last Modified: Tue, 20 Jan 2026 18:52:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:94f8e027818906985d62d5d97fe55f9415f1e28cd9ed7ef76a5b85daa211e043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a87d96ae295306037cabebf1a1b57745367911e73797c19263f3edcff8dbc3`

```dockerfile
```

-	Layers:
	-	`sha256:76ef31a76b30e8eece48d35bd9d2ecdfecd28e2aa8c77da0ef80a1257e2aa6cc`  
		Last Modified: Tue, 20 Jan 2026 18:52:06 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e83ef1f24753c7af5b8814f0e69c4399b7005e29602e25b3153a201a680b8555`  
		Last Modified: Tue, 20 Jan 2026 21:24:49 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:505f7e823da28ba996053949b66d41265782074b1cbe41934fb184ebb480825b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96858765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870da551171f2ad530df378f1bf7ffa755642582d44408f4aef2c911435e0f19`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:53:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:52:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:52:23 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:52:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:52:23 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:55:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:55:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bd1a59a74e07875622ae7c83765b0ac84050a2d500be62b21ec7d22f9ea7d3`  
		Last Modified: Tue, 20 Jan 2026 18:55:23 GMT  
		Size: 291.6 KB (291634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2898920cb13c505259be6cf40bfc2b763657f2a33b173994b269e661d72ebfad`  
		Last Modified: Tue, 20 Jan 2026 18:52:52 GMT  
		Size: 92.9 MB (92948041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56389ccbc053d71be31961fa60dbbd6d66836615d8d93a4205c3d2ac72cf16a`  
		Last Modified: Tue, 20 Jan 2026 18:55:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:647fc4ac5db785b70a08cd96a76a9e9c828982d51bda01d74fc11cdac3c903c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24f936283b7ac88b9cf01bd2e693e456eec4f66ad7703b52f8850260b229105`

```dockerfile
```

-	Layers:
	-	`sha256:7f6fed520365204bbb785b31534f6211b1aa1f26aac96e69f949ec87bb29c7e8`  
		Last Modified: Tue, 20 Jan 2026 21:25:16 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772996998438fe3e89bfee5eb474c4f364484f00a8df56f53bffe80cdebb2464`  
		Last Modified: Tue, 20 Jan 2026 21:24:54 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:bc8552f6d971ec07303a58b34f2b3def3ef9965930b3b95ed535b44131ef1873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95708847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18409a031ca467e5d4f89f270ab905c48e5d90d215114b49574d3e1eff09896`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:54:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:54:57 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:54:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:54:57 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 19:02:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 19:02:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daa35feb63e7ef5c9399e73cf4420af92b3279e1deb9e79d9f88735b792386c`  
		Last Modified: Tue, 20 Jan 2026 18:57:07 GMT  
		Size: 91.7 MB (91681857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2760510723ed5bf7fb212d8bc12dcd8b2633dcb38c1f321746e05f701b18ebc`  
		Last Modified: Tue, 20 Jan 2026 19:02:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:d24fd76626ff4918bc98a55e4549c61fa39db8c5496d4c92a00861eed92ec0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819cce84826a79e918fd38c46846850c391ae0ca27f2946d5252c1e95507ff1e`

```dockerfile
```

-	Layers:
	-	`sha256:0aa0f185090ee0192388410fa4c80660c204fd29c30139c8b67257eb90bdba10`  
		Last Modified: Tue, 20 Jan 2026 19:02:34 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d8ad4f5bad2ffc48d9a09d8e32f1b5f732abce5b64f1bde626265d4f88c4c3b`  
		Last Modified: Tue, 20 Jan 2026 21:24:57 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:b9457f6ae0c7f111c5ea3ae1430820e1f813d2c86af72c464d58981cbf5a2bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96122798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0353ff8633b1dfdfaf37bb60f91e7e9b85b3455180edb4be3cd0dc1c196f71`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOPATH=/go
# Mon, 19 Jan 2026 21:38:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 21:38:33 GMT
COPY /target/ / # buildkit
# Mon, 19 Jan 2026 22:18:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 Jan 2026 22:18:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:12 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a3cc83856871e3a177f0a6b27128217f73d5993c49818bd1374bd92a6bcb48`  
		Last Modified: Wed, 14 Jan 2026 03:12:04 GMT  
		Size: 92.3 MB (92315877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a19461d8b4bb7bb1df143516b4b1640d2ef9f1dc9a2ceab2ed0635e03d666ef`  
		Last Modified: Mon, 19 Jan 2026 22:20:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:66c5197accf41705df3641327bb3c170d8a8e965b152bb85f869b9c769b7bad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b113429ee2bfac29475a5848e3f21c00bb8ddea9d90c1d2f17d89c06cb74cb`

```dockerfile
```

-	Layers:
	-	`sha256:4ef9240ee899ee41cb5f79ea30548a0a0a3e9d3447c0171a9ef50bb5e8ff1e8e`  
		Last Modified: Tue, 20 Jan 2026 00:23:59 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a381386b0e5e7cab0e2cbeefa77be91302b01415012a6927f8ab5ecd0b609d8`  
		Last Modified: Tue, 20 Jan 2026 00:24:07 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:a7671dae7cbf4b0e5ab8a4d90c2c2882dfe7d3f585e4570e69bd7ea38ba41527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98174241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada5a661cf9de0a424b13c7f1da6f7ddb45476630447bfa6d98cb7e1476df564`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:29:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:53:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:53:23 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:53:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:53:23 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9d29ef25b91c67ee1e00545a6d668d3bac1c38574e667175946c9679a1b62`  
		Last Modified: Thu, 15 Jan 2026 19:30:15 GMT  
		Size: 292.2 KB (292153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee8ceecb5a37e7411922ba0485d5dd3cc40ab1953ffe651cbe56f40f79a249b`  
		Last Modified: Tue, 20 Jan 2026 18:53:53 GMT  
		Size: 94.2 MB (94232686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cb7f0b5ffdb6cfd032631ce3cf92ae18d142c06d3c2f59c057786d14c3b9cf`  
		Last Modified: Tue, 20 Jan 2026 18:53:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ebbfc0e1d75e4d4c50abc347c9094711cb3249a03eeac5ee24b965aa78b1d09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b290f88633ac492329892dcb39001221aed3b8f0b059dbe2a042426cc5709d2`

```dockerfile
```

-	Layers:
	-	`sha256:a39f8f1daed9955d775def424210902ac29a9c63cf2aa95ed488869028707450`  
		Last Modified: Tue, 20 Jan 2026 21:25:22 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0552d33de69bf00e0d6af295098a37168ce3a50594c73d02bdf54bf38c8b36a9`  
		Last Modified: Tue, 20 Jan 2026 18:53:51 GMT  
		Size: 24.3 KB (24292 bytes)  
		MIME: application/vnd.in-toto+json
