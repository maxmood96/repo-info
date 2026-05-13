## `golang:tip-20260510-alpine`

```console
$ docker pull golang@sha256:7b144fdebaa728721579fc0869235c7f585ad4ad997852e9d2ec78a10232d83d
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

### `golang:tip-20260510-alpine` - linux; amd64

```console
$ docker pull golang@sha256:e552ef6f6f698ea75db501b8fa1a58e5b6b7c9fa9659e9bc523a261d35c34026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101570992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a1da223af9347a10963b7652604088356cba91d60964f8d8a6d2383791d243`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:24:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 May 2026 23:23:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:23:39 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:23:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:23:39 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:26:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:26:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383dc2f6f8fbcf6c83e4905f83195e0a0ed955891285697135948164250c1909`  
		Last Modified: Mon, 11 May 2026 23:26:31 GMT  
		Size: 290.2 KB (290243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970dd4e15afd4dda5f0073081cf90c52ecab4076d0f8b775deea9b5b1305744d`  
		Last Modified: Mon, 11 May 2026 23:24:11 GMT  
		Size: 97.4 MB (97416403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7233919579799d4dd7621f799bfcd20b766c9bf671be0244ff18e702f7834a24`  
		Last Modified: Mon, 11 May 2026 23:26:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:285cfe28b67e12ab1ce2d4efc55d084100c7bb1655525f8c32d28adc77e0f156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ccc8c838a278a322f581c7ad224ebed3a32f49be850a413a7ffef60bf01ecf`

```dockerfile
```

-	Layers:
	-	`sha256:d6196ee9774ab285a1c929afb92b40deadfa223bf1493511adc84455fa7996a2`  
		Last Modified: Mon, 11 May 2026 23:26:31 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1922b510d60df4514e1ce4e06f7344dbc1412f6e0ba9b6e67cdf305ddf7205`  
		Last Modified: Mon, 11 May 2026 23:26:31 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:d4a829cac39f4b04ffbf290d2ad6651dd83d216aeb063f299672c90c071bb0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97391338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af9ea4c18f76b54756abd9cc2e777b0c65f5cb1f69ea06ce00d72d790fb227`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:21:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 May 2026 23:24:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:24:29 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:24:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:24:29 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:24:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:24:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442bd1ea5fa0653d07e126ea3b3f3360ae28bafd86447d332afc45f1ecb43612`  
		Last Modified: Mon, 11 May 2026 23:24:44 GMT  
		Size: 291.0 KB (291028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85b58750c4c9c6ff7bcb713a183342bb0bf05cafde73a18ecc5ab9ddb9b667`  
		Last Modified: Mon, 11 May 2026 23:24:45 GMT  
		Size: 93.5 MB (93528289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91af4b13aa50bc189b6b246cfca2a2453c03127654d65efbb71297de32e39ef`  
		Last Modified: Mon, 11 May 2026 23:24:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:36562d9dc6efb5f16b6ff7a490672b777de197e96fce51ffde06330886fc4176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c19dd2ca5bfe58e0d5cb6f49720ba515a32ee2da78fd0852e3bc71f4f0ccce7`

```dockerfile
```

-	Layers:
	-	`sha256:8a9b8e9f1225daf429e928131e11ee6a5eec36bfbe334ebe9ba20e4e8b97c580`  
		Last Modified: Mon, 11 May 2026 23:24:43 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:8c795e495f67d30458ccaa65ea4142dda1da43dd8cf990c6bbe43a11b3ec746f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96828669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd8213c44118f7d7a981db220b9df12fc062245b5e3544409cf32baf60215c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:31:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 May 2026 23:34:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:34:28 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:34:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:34:28 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:34:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:34:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb23383102c588fe46d08a9ad9e43d0963b3f7d62f01272ca3b084a137b98be`  
		Last Modified: Mon, 11 May 2026 23:34:46 GMT  
		Size: 290.2 KB (290167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5a325591cc56f1ee0a299253454b588317de6e43dc9dde0447e3b98aa2508`  
		Last Modified: Mon, 11 May 2026 23:34:36 GMT  
		Size: 93.3 MB (93255222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e40c5fa6ba847c35daa8bc0b786f0efb92dafc139d6b1fd256e48536477d3f7`  
		Last Modified: Mon, 11 May 2026 23:34:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ec9e727956f0358f11ada8c873eacefd06a139bd37b76c12c81539c71479c108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d810fa5804fa18d156081ab6106284557069e9c6723f3bbef0605316da5e886`

```dockerfile
```

-	Layers:
	-	`sha256:e9ab1c707d461e4f319323682b8a1d1450009fa0f6a64d48541b727495284df1`  
		Last Modified: Mon, 11 May 2026 23:34:46 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3985156a0c38f9ae0cc10d537bcfda3b44b31edacc8747f4db3482cf4d646b`  
		Last Modified: Mon, 11 May 2026 23:34:46 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9105e126e316a81a05455a5d32705b04de6d44bf71088bb7c63b10262de7c3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96616122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b80e10a6b3cfe4892b65d7e874d038e86d3c9f157302914483a6b8f8505b0d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:24:36 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 May 2026 23:23:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:23:57 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:23:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:23:57 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:26:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:26:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3a708326f24a11ebc48da9056dd48c8a49842b72052989179e7e4a28f8e89d`  
		Last Modified: Mon, 11 May 2026 23:26:30 GMT  
		Size: 292.9 KB (292867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff2fbc71fe7b87fac66a8dadd85dade8191c7b4ae8add0914f8708f3a3fd259`  
		Last Modified: Mon, 11 May 2026 23:24:28 GMT  
		Size: 92.1 MB (92123227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43caadc3eb373c0aff7d07e1037ff02dd7f6607d30b5d25505c3fe6ac7b5fc6d`  
		Last Modified: Mon, 11 May 2026 23:26:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4d97b90d30d712525691d00a47232ebf0e4274346cab5db3d307099d77febcf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f310b6766c004caec2a0aabf0e7808def1afa12b4c5e44be6a9c6e80ae7a3f3e`

```dockerfile
```

-	Layers:
	-	`sha256:5b02e44cd63eedc6ab2b3def3dc841f692a0a2635c113f1384c5d4a370df1a75`  
		Last Modified: Mon, 11 May 2026 23:26:30 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2e25be274d79dda47a091e06cf1877faab0ff415a90bbd63b1e2e0240bd145`  
		Last Modified: Mon, 11 May 2026 23:26:30 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-alpine` - linux; 386

```console
$ docker pull golang@sha256:884cb7ddf1fb890b6660388e01735f37c46e0968e134ab2164766676ca446150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99156101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9af9abb49fea76d2b6fa9e2b35f9a97f6532e361269aa406192421f379c7a6b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:27:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 May 2026 23:29:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:29:33 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:29:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:29:33 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:29:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41e06a0ccfd9cb682bbf287ca8d992132b07bce347af2c8eddc450d346b906`  
		Last Modified: Mon, 11 May 2026 23:29:49 GMT  
		Size: 290.6 KB (290630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf08a2b699c1c99de16bf0901d8891e91bf0fcf2a4afdcaef52c57556a2e35`  
		Last Modified: Mon, 11 May 2026 23:29:39 GMT  
		Size: 95.2 MB (95174868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9338584a9c5bc792ad0eac2a4642bb47af88e3626d8367952083d83bbf36c`  
		Last Modified: Mon, 11 May 2026 23:29:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ed007cc4709975c217e18380b79c60928f1ff541263e9c133e357b2cc3e7191a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c9801bef11a11b1232f93f0caf1469ebe2b6b05a8cf3d521f1f29a054da28e`

```dockerfile
```

-	Layers:
	-	`sha256:597a2d260fd8c4abbfa343ac3817373c082c5a2fca18e339cce2099e15a5299b`  
		Last Modified: Mon, 11 May 2026 23:29:49 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80987db1822fcf63241c0543cf083ebb2344ef2d4d5c8fc399b4885ff5af7be7`  
		Last Modified: Mon, 11 May 2026 23:29:49 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:e745449e12342be5ba04f3b33afaceb790133114f3ff3cb7f1c90bffe9ff6073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98103815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583c50c7a2f3de19a6a8a4a7ece2f22772ca10ec9e024e0586bf98fd5bea0f35`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:47:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 May 2026 00:42:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 May 2026 00:42:13 GMT
ENV GOPATH=/go
# Tue, 12 May 2026 00:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:42:13 GMT
COPY /target/ / # buildkit
# Tue, 12 May 2026 00:47:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 May 2026 00:47:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3404ddb9c665ea1e1f42e9894286fa3caedc18a9e1d221140b6a000d044639b4`  
		Last Modified: Tue, 12 May 2026 00:47:45 GMT  
		Size: 293.5 KB (293453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c0dd6efbd44f19e1e0d6c48f823bb7238da1300bf904818347619de09b8359`  
		Last Modified: Tue, 12 May 2026 00:43:15 GMT  
		Size: 94.0 MB (93979275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6ec08af8e8a6d8be1965e9e63288b11165d23fd1cc7b268b9ff4b20a000e2`  
		Last Modified: Tue, 12 May 2026 00:47:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1b87f84739540dbcfaacb8626ccb41391402518f8a0f398e2633b19534386d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 KB (218026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986e3a8e3ea7638540e7c9651e1c5ea9f2600d110ac6f42516dcd9fe02ae186c`

```dockerfile
```

-	Layers:
	-	`sha256:1d03842a16e9b3a481f998749b2fe8f9110cba8150403567e83574562a5efa36`  
		Last Modified: Tue, 12 May 2026 00:47:45 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f836b19563e0227bfae0d3db917486962a10271bde3899f2b6f2863df17c0b`  
		Last Modified: Tue, 12 May 2026 00:47:45 GMT  
		Size: 25.0 KB (24979 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:d34fca002e6feda3b93eee5a10f37b1e6543f37668f0b6a8bf19961fe76a9eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98383785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21df12c98ac1fe7a90384833f08ec392ad063474254cd29ffa563ab50681cdd7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 13 May 2026 16:08:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 13 May 2026 16:08:37 GMT
ENV GOPATH=/go
# Wed, 13 May 2026 16:08:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2026 16:08:37 GMT
COPY /target/ / # buildkit
# Wed, 13 May 2026 16:08:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 13 May 2026 16:08:55 GMT
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
	-	`sha256:d38d47e378dbd0b7bf645831e9840670b418c2e00a7d67e6b9db247ed04df4c4`  
		Last Modified: Wed, 13 May 2026 16:12:01 GMT  
		Size: 94.5 MB (94505412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d79090c590d5c23b02b0fc71b74b1709e31dbc53eeb7d1c3030e6826279bda6`  
		Last Modified: Wed, 13 May 2026 16:11:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:33728962a61bd0e8f05d5e319208a22fc3895b8a869831ebcf58e8f2870b462e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeee1be69bc46bd23b99574b02ad4d748d69c25241900c81c43b2551e8a10ce`

```dockerfile
```

-	Layers:
	-	`sha256:bde41f5a0d5aceee7936f3421261f4cc5e181152d3e2fb3fd03400978af06030`  
		Last Modified: Wed, 13 May 2026 16:11:46 GMT  
		Size: 193.0 KB (193043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77a2b1f6e327a2590b4e65f20db0a7fe2beb8d6dd488dea8faf1ce6ffbe3767`  
		Last Modified: Wed, 13 May 2026 16:11:46 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-alpine` - linux; s390x

```console
$ docker pull golang@sha256:b5fdcaa50ab5460780531081e933f1ad7c96bf1c8aa68149a7b7dc458d5441ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99966049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8faeb7b8631b5e7671771f254307443e669c2fabca9f468c7526ad7d1863bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:26:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 May 2026 23:26:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:26:01 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:26:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:26:01 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:26:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:26:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6b712f63cd2eed21583a59ccc1eb52a21d98f1c14fdab28d621876262bcb3e`  
		Last Modified: Mon, 11 May 2026 23:26:32 GMT  
		Size: 291.2 KB (291158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccba99e1a42acaee11681a55a3c5791d533460e7e22dee60816a7d3a0553d4c0`  
		Last Modified: Mon, 11 May 2026 23:26:26 GMT  
		Size: 95.9 MB (95948201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c11dc699c7ac1010caee0436b73371b104f32035441bd4e3a5734900347d641`  
		Last Modified: Mon, 11 May 2026 23:26:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8a1dbfed04746cd2d0b7d72c89537252bc58f40b9be018f022090788cd86d756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cf1eeaed03afeb2eb1718caaee8a36010ea3c7c3073ac54828449ec6ce2f18`

```dockerfile
```

-	Layers:
	-	`sha256:5a4f283c30719d048064300df7d6f929cfbcae1c43c050d87c1d86f587e342ee`  
		Last Modified: Mon, 11 May 2026 23:26:32 GMT  
		Size: 193.7 KB (193745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0758a47eab1679ccc913f0d1bd15a983b02b45e276396ba92289be4444759048`  
		Last Modified: Mon, 11 May 2026 23:26:32 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
