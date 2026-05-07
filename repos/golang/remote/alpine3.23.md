## `golang:alpine3.23`

```console
$ docker pull golang@sha256:91eda9776261207ea25fd06b5b7fed8d397dd2c0a283e77f2ab6e91bfa71079d
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

### `golang:alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:f44b851aa23dfa219d18db6eab743203245429d355cb619cf96a2ffe2a84ba7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71439667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fbd9862b05789bb9e5462bf7d67300660e2ab5217aeb637b8db103ac45ea21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:37:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:36:58 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:36:58 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:36:58 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:36:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:36:58 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:37:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:37:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17423c887b377ec28c3923bc88337384a7a0c1f2b50b7faf4912760e8d503ebb`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 290.2 KB (290240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70bdedd442d430ea119cf8db8c0031b4eedeb5bde886892773876ded7629e8`  
		Last Modified: Thu, 07 May 2026 17:37:31 GMT  
		Size: 67.3 MB (67285082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1512b43389a873b0519ae3d6c1a3c4d9b19295b8e3330b040d95d73c50ba2f9e`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:f5fed3f8c50eb5aaf519c395c9b5eab00ac256522c55c1b338d65090147bc29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f218850ada7e7b643deda2d7aa2b46c6068ceb3ebb5acc28461a33f6c74c9d0d`

```dockerfile
```

-	Layers:
	-	`sha256:d0e37aca80016b1fdb4a73ff3fe88b6915ce5ef62de54ec8ced955c8c0287f42`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 195.1 KB (195068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcb22212809db82a5a09e485c1f61910ccb71af283340c0b4fd9664772668fc`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:22f41c3ea76b5c9e0df16e3798f67516265a22a4d1096025586904282204ae15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69649571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f12a82e396f6b05a90840d39181451bd0d79bc8e817be7c9e6a274f77550f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:56:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:56:53 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:56:53 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:56:53 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:56:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:56:53 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:56:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:56:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687009092f42112fe3060ede6d29f6140685d07bebd8ce3ea35a0e9641d52139`  
		Last Modified: Thu, 07 May 2026 17:57:07 GMT  
		Size: 291.0 KB (291027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323b6bdac241fc54c2e0e06ca7f4045ec740c882bb235caa36f634f6857573cd`  
		Last Modified: Thu, 07 May 2026 17:57:09 GMT  
		Size: 65.8 MB (65786523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdf014bd07811d672a2f4f8f1dfc9d69bb5aaea6fd7943530bece2bcc12c3f8`  
		Last Modified: Thu, 07 May 2026 17:57:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:4980071246b22d9b56805f79f5b931805470d761dfa632ee74a5295fc6efe876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068a50158635b67a2ea35b1bc877485f01b22c16843d4972b58adb3fe1f151b`

```dockerfile
```

-	Layers:
	-	`sha256:a24a9e1db2b2cad611e570d47cda34d89bfb80a2d577a9e546b20a4792eeb6c8`  
		Last Modified: Thu, 07 May 2026 17:57:07 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:5844c2a183cb1687688db3a4949c243023589274fef6a7eef4dffd4bdf5b4a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69359921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b561d9d867176c169237ce25f4e3f0ec84ce8d4ff79651d3428e6bf07df4b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 18:01:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:01:29 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:01:29 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:01:29 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:01:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:01:29 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:01:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:01:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edfdc54fc8b2d0bd0428faa39d6e4e185d5561d50ba518340fae16d2e464d2e`  
		Last Modified: Thu, 07 May 2026 18:01:47 GMT  
		Size: 290.2 KB (290164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e7137c96fc07d2fc9e87f7cec43a327dd6c1385057f6c469907ef731cca2c`  
		Last Modified: Thu, 07 May 2026 18:01:49 GMT  
		Size: 65.8 MB (65786476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1a80c7896f8a764b0302d7643726ecf90ebdd66bc34ddaccaed3b25748d797`  
		Last Modified: Thu, 07 May 2026 18:01:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:3a971b2291cfdc1960a6e388e94b8eef25d256b0e26b5193d13ef0775a8f58ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bc31d17d1b81c55948f1ae7f3dae19df7172846c2cad7add5ea3cc987208e0`

```dockerfile
```

-	Layers:
	-	`sha256:4694c97387bac7de183243b16db9a623315257e8f0c21a5dbe8788ae6c3e3e15`  
		Last Modified: Thu, 07 May 2026 18:01:46 GMT  
		Size: 194.5 KB (194470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6281758317307f32d263c32a1477ffa8d9a3343999a5799afb85871a738c9ad7`  
		Last Modified: Thu, 07 May 2026 18:01:46 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:91dea08171115da4e00f7a5c74753c4e56f4e83e20b1e4065530b5d51d93742c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68660668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85526332edf09ad0a0c7acd875548d5b04a98e08ae64272efa724b244eb1c91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:42:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:42:16 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:42:16 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:42:16 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:42:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:42:16 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:43:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:43:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef948c355a7dc83c698cdbb853ce74cbea62b03bcdffec75a5ddd8453edb8fcc`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 292.9 KB (292856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fa76ba696f7dc4b9e2330d4ae7c03a0f4b2c055caa94b353f7f600a6dab0c6`  
		Last Modified: Thu, 07 May 2026 17:42:45 GMT  
		Size: 64.2 MB (64167785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e696fa36d88793f0869c86c611ba1d605ad3a2a7f60d00018579c8c2c9f935`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:a305b1da5eca73ac7d25e3dc8ea1734aa9a5533d165074bb0f449d62bd6984ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a41458ebb8c0d4e4db4126a9562316825236120eb86a232aba00bfd2cb203a6`

```dockerfile
```

-	Layers:
	-	`sha256:8f9b522dd6982502968f41aa37e38e8a3c8f7361e8c29f4e4b01f9297a199eeb`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 194.5 KB (194522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270caa600e6a9cde106c930b3d2a0a74333878a31f41dd3c19b66a6fb948cfc2`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:3a8f055e02fce9585d5e4ab5135d57f2e1a947a16e2a7e6a71a78e770c169e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69580386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff423aff05c212943d624a9fa8e6c44e45d506e06681eb8b3c52350e3baff1af`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:37:59 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:37:59 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:37:59 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:37:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:37:59 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:38:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:38:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff356be0868643267e7ef13fa541a4ed3de24ebd1cefe71fd5fd4a40c12ef7`  
		Last Modified: Thu, 07 May 2026 17:38:15 GMT  
		Size: 290.6 KB (290635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40fc8fcc10ee56c441c06327bcf95af166f71835205a4f4eff05758add1ec7`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 65.6 MB (65599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c134aaa6e81871cffc95032d2d94333ad68a39d4fb0570a177ed316490359c`  
		Last Modified: Thu, 07 May 2026 17:38:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:388d5e136b25c992bc0ca2055a5a08b842fcdf22274fbeae5c65f34c44ad2319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 KB (220978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7599c93ffa074c9fec66bb05ef7f72301b0745dd1ff9cbcedf68d4569f2674e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f2bb6e02ba8b65c9ca9d4c42153b747425053d1e4a9a437745a13088fa477be`  
		Last Modified: Thu, 07 May 2026 17:38:15 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93de6a79e3a2990178addd1d86823a9cea257b2920f66486d3d83f23c451d7ba`  
		Last Modified: Thu, 07 May 2026 17:38:15 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:321a841d4d8005f29a873ab46acb9b95f16afaa06328aa5dc6d55c831e765a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68967144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2465a25368a124216f78c40e42db26b1b0a33603cd24ad5168e54a404d9c38ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:19:35 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:19:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:19:35 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:19:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:19:35 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:20:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:20:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677743e4af652dd79f8723ff89a284363d59474b87d72b559faf60d691a51c58`  
		Last Modified: Thu, 07 May 2026 18:20:28 GMT  
		Size: 64.8 MB (64842692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee189eb7d23e0eb2e86ca34b7830e767dbf97b024834fd7fdd0ab530d805c638`  
		Last Modified: Thu, 07 May 2026 18:21:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:ad01372dfb2945e57452b262b5cd3e142c4e805b739c6568c9111855cefc062a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bc9474b31fff2d3f87bc4ae766450f302e81d91fd596457d411562f4ef0510`

```dockerfile
```

-	Layers:
	-	`sha256:2585f8d1024916df484f55e0357233cb3acce7e330f39bf405204f86eb996781`  
		Last Modified: Thu, 07 May 2026 18:21:06 GMT  
		Size: 194.5 KB (194491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d09fec66dd82491fdba54c0f6f626943e8c0caff8240dc280f1b71647d293e4e`  
		Last Modified: Thu, 07 May 2026 18:21:06 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:b00f98137c686687ae4fc08f67ba1a40c26f4d5881b49af4823aff13c24de850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69027847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b4d7b791511461497ee8bbcf8fa48beb89e55966dd4a22f4564b2599cd8394`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:25:59 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:25:59 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:25:59 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:25:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:25:59 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:34:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:34:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4576730cc1188381475a15201ad7de7153b28247376e0d104bbac61494efc78b`  
		Last Modified: Thu, 07 May 2026 18:32:41 GMT  
		Size: 65.1 MB (65149474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01f520b0871630b1aa35b312ac2ae6237ed1b369b8d20fd9ff81da0108c9a42`  
		Last Modified: Thu, 07 May 2026 18:35:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d726c11aa8f1350e281f06cb4eee6a69f1ec17d2d453c07d128872b225afd6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8a1bb8b67726fda54f691fa90a6ae9cb6302b691bde49d10628bb61578a789`

```dockerfile
```

-	Layers:
	-	`sha256:b428991de4c6ad4df456b5d01360d92bfbbacaa78f5a64ab4e0e03d2db34c47a`  
		Last Modified: Thu, 07 May 2026 18:35:35 GMT  
		Size: 194.5 KB (194487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442906b206e55abe41eb20dc50b0014250f5e124e4ba2fc0a727840eaabbb916`  
		Last Modified: Thu, 07 May 2026 18:35:35 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:29bb2334128cdc233999402f131b45281c66b45cdab9f9eeb095c3c970c7610c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70533965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a857156823ef9efc846049db3ad0be9325957926dd42d8d818a8d5a48e9e2d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:34:39 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:34:39 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:34:39 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:34:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:34:39 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:34:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:34:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb85227a6d474422f642a20f11c0f9c523b2abb74d9032c4b7170dedd36bf4`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585ea404f5b1266beca471637498b2c7b5b5d49eff5d438b1d1e375a59498340`  
		Last Modified: Thu, 07 May 2026 18:35:38 GMT  
		Size: 66.5 MB (66516126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370826142cd9242ae85e8b52042350257ebd60c341f40fdab0c6adc7129cc4b3`  
		Last Modified: Thu, 07 May 2026 18:35:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:72080f54c08a559a9059cf533cededd7f572240de6cc224cece8ff209e812163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b28b062ea309214537b58694b1a2d899e7b18a614a3298869dc6793dc413412`

```dockerfile
```

-	Layers:
	-	`sha256:2c85c9f93bf0385c9647213b5004627f9dbe0ff4a427f82762a120b5e798e908`  
		Last Modified: Thu, 07 May 2026 18:35:31 GMT  
		Size: 194.4 KB (194417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7177b7dbc5592ad817114ad4508961fb404dc6a46263a8bea8611da3200954e1`  
		Last Modified: Thu, 07 May 2026 18:35:31 GMT  
		Size: 25.9 KB (25854 bytes)  
		MIME: application/vnd.in-toto+json
