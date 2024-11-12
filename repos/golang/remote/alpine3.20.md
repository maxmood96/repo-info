## `golang:alpine3.20`

```console
$ docker pull golang@sha256:c5eb6fec061d27450aca04855e80d4c78b745c94db1431f8ea5459f56fc24577
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

### `golang:alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:03bea3386a1427e9de21b9278fdcf8a3941d41b92498866a47a91fe15cbf1dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77953946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98069ee7ef5d97727559513880f76a2de6a1656a51f3685e074309a1b14f7718`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5418e60db87de98b06e455a400579c7f27106374f3450aef2951989cf6c7f536`  
		Last Modified: Tue, 12 Nov 2024 02:13:18 GMT  
		Size: 290.9 KB (290885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79bddf330f7de2b96b69740174bc7152350ef81439db2dfa776fc3a9365dc80`  
		Last Modified: Thu, 07 Nov 2024 02:59:16 GMT  
		Size: 74.0 MB (74038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f115f9222c8e1a0a23300412608c2f4a3d45a6a471af693ed24f073d76d9f288`  
		Last Modified: Tue, 12 Nov 2024 02:13:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e4a327af05317b308d6fcbfcedfd7cf4a46193dc275e9bfce8db6099bc9610fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 KB (236111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7977c43875739a9411099462f3cdb675191e8719762bf9f2dfb668f4760e2b`

```dockerfile
```

-	Layers:
	-	`sha256:f083dc7c3ae2b9548380b7085dee8e54f12e07d113201afacf55cffacf937921`  
		Last Modified: Tue, 12 Nov 2024 02:13:18 GMT  
		Size: 210.0 KB (210042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc402d25cb930eb6e20ee7b477585cd9bb8b5d160a3b095dfaf78801d41dadfa`  
		Last Modified: Tue, 12 Nov 2024 02:13:18 GMT  
		Size: 26.1 KB (26069 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:aff1a3076b85ca725ab3075f8fe96fa6d39b1aa77ec8a312420b07549ba35fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75842369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097e9c9a254bc7c2c025d6e9ac4c20cc0a0d211670bd07dd143877201a7cbd3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b15e82573debca2fd0fd40f07ac032fefe7f9180bd45f4f9cf2c2afde7d486`  
		Last Modified: Sat, 07 Sep 2024 02:30:42 GMT  
		Size: 291.8 KB (291766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6930abd3e962e7fc186f25f91e441a0655bacbb61cdd3456fbbb1368d3ebbb4`  
		Last Modified: Thu, 07 Nov 2024 02:59:03 GMT  
		Size: 72.2 MB (72183939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cbd67afa5dce215f171ef96e6a8c433a7fa35da4056ea98d54c33154aa16ac`  
		Last Modified: Thu, 07 Nov 2024 02:59:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:fd86106870062b91f3f7cbe74325fa4ff4b54a24590cb1f4ec5a9908e52035d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a9abba53a8ad91c05b474cd823fb723dad305cd43dd7e787db694eea8f7ee8`

```dockerfile
```

-	Layers:
	-	`sha256:f4c4a4e547b49ec705099a715d2f65c2416027a1cf12897f9b55c3a4614051b0`  
		Last Modified: Thu, 07 Nov 2024 02:59:01 GMT  
		Size: 25.8 KB (25790 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:8bf187a4a3af616ed0596d06a81a3ff3fb5fd9a51bae4ea6ed00293e2b5bfb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75570705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8a01b3ccf9c466308f8be4005cad2777d16553ef01623504f3901f99f62b62`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692a5c99cf15c99e5e68f32ee94771988d92aa96b54f7c87c6ca7ecd4a4c3ef9`  
		Last Modified: Thu, 07 Nov 2024 03:01:47 GMT  
		Size: 291.0 KB (290959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e990400f8c0342109351b2ea2dff891387190e755f29d02b0f474578fc3d222`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 72.2 MB (72184086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251afc28a17b6c762e549530d05085933556f149eecfe4bca0301753743f37db`  
		Last Modified: Thu, 07 Nov 2024 03:01:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:676cf64609116f4bdd486c96d161e6c73ca49f8bd1b5e2573b435b09de54bd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 KB (236079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca1c96d98609e0ad481e1e5ef48623d6f15ac66d20ab4779386e33dad6dc1e1`

```dockerfile
```

-	Layers:
	-	`sha256:2d627d4722c4e9fede68c0ecf5c14a58be6fa8f759e6b29972af9d6ba3304cbf`  
		Last Modified: Thu, 07 Nov 2024 03:01:47 GMT  
		Size: 210.1 KB (210074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a33ef8c09259f723797a1916943f631d7954139a787494054bcd205e087ef18`  
		Last Modified: Thu, 07 Nov 2024 03:01:47 GMT  
		Size: 26.0 KB (26005 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d2b883c6b473da95c418cabbd576d54e6e071f7541e381e497fdda0e2ae5ee7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75050280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329834fefb2a45fbfc46c07a37281c608bc65d48aad332cc97f8cfe8afdce132`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a9dd7d6fc256d156365346b32d280a887ef75129be8a63ce1612b621fc9714`  
		Last Modified: Thu, 07 Nov 2024 03:00:57 GMT  
		Size: 293.5 KB (293527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cf7f03564cac6b07fdbe6eaff976145adcb2737e465abf5d0c66ea7d293a11`  
		Last Modified: Thu, 07 Nov 2024 03:00:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:fd9f4c14ba1a3cb8cc6999fbfe2ee0a2dfbe783207f4f967249ca9381d4c7861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 KB (236198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8535118c1a727d08dc8c98abefa3d032eefcd632e48274539862892431e5180c`

```dockerfile
```

-	Layers:
	-	`sha256:565e5ec4a3f5d3938bffee4d7c5554aa6419fecc82ab754a79748c19984d3abd`  
		Last Modified: Thu, 07 Nov 2024 03:00:56 GMT  
		Size: 210.1 KB (210146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cb6b1dad24345b3034c4427f116bf6a04826af426d04b4a1e810b8f4559609`  
		Last Modified: Thu, 07 Nov 2024 03:00:56 GMT  
		Size: 26.1 KB (26052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:cdb47cf7cc930903987ead22e38dfb607db077bf120e740f7f5f14d1d18e4668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75668757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fad2811aabfb55ef3386374577d6266dcac66d0e8ccaa067d778f40fd02852`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e0f41ff967264bc14bc9161ace5c7494387e43fad5a39cb97f6b11be85c322`  
		Last Modified: Tue, 12 Nov 2024 02:13:25 GMT  
		Size: 291.4 KB (291364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d309da02a5efef0a1926ae8de3247932524a303115a90abb23504c4cffb291`  
		Last Modified: Thu, 07 Nov 2024 02:59:09 GMT  
		Size: 71.9 MB (71908016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac9098bc0f60c9077a6aa3780b424692235a9f9dbdeb39710a66e8fb3f8681a`  
		Last Modified: Tue, 12 Nov 2024 02:13:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:cfc1a621ca770af0f0ad92b075a558f43f7fa99f52d7acae9a6d5da5ec36bbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 KB (235975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5af7cb69f4b1d66a9408dbe403b3decdc36a0f358d84b3ebd3f507fcb34e3de`

```dockerfile
```

-	Layers:
	-	`sha256:3f0c049525ac405e85ed6555cbcabd189f7feadd57b82fb1ddc7fabb81daf7a4`  
		Last Modified: Tue, 12 Nov 2024 02:13:25 GMT  
		Size: 210.0 KB (209961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d22276fc42f201f5f5af6d3822bbcc3d3fe91ab854216a96bf3e4b9278806b4`  
		Last Modified: Tue, 12 Nov 2024 02:13:24 GMT  
		Size: 26.0 KB (26014 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:37f9c292350435b6918f2b3f13242b2bcca7f1ae066f0dc8149601b40a29a564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74695090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7fc040b23e49f073c05918a8dcf874dcce65537fdf8a9f9a9ed55b61c0716a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977bd9456f1b6f8f4f6980e045da412051b1eade2ac61e6b8469b4da52c93c14`  
		Last Modified: Thu, 07 Nov 2024 03:00:59 GMT  
		Size: 294.0 KB (294035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575d60aafb46a5e5a1ed1b28ef7df9a44a573432b2679198eaecf6dff5d9a40e`  
		Last Modified: Thu, 07 Nov 2024 03:00:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:f6902304c020dbcf9bfdecdd7c6f1bbe9c90c70c5273d83a57a1529ff90121d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 KB (234125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270e30b8c7aeac5f29192cddf50408a147ea1e4f11b96eaac1f14284d4fa827c`

```dockerfile
```

-	Layers:
	-	`sha256:66fd37498fd63befe06bb385edea933addb76b9036fb5efefe06062ecc3943f6`  
		Last Modified: Thu, 07 Nov 2024 03:00:59 GMT  
		Size: 208.2 KB (208182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe82abddc4074ab9c43a199dff7dc67379d0055eee3292435d1ac0a12e4417c2`  
		Last Modified: Thu, 07 Nov 2024 03:00:59 GMT  
		Size: 25.9 KB (25943 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:71b8e7aa6119277583bb92a3b612af8a0f1976cf3bee0b45e2770639750e7449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74890430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7040f7f3adf7d411011f316834a01078adb28e0e66101ad8011125b13bab7cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d1647e2ae8eb941891fcb716820e5bec12b348afc0d29dbe6ad642a22cf24a`  
		Last Modified: Sat, 07 Sep 2024 18:50:29 GMT  
		Size: 291.7 KB (291675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c484c4d08cd9e67227d89dc190049950041d21e09449643180abb682468f67`  
		Last Modified: Thu, 07 Nov 2024 03:03:27 GMT  
		Size: 71.2 MB (71227144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc55b235be95f2ff6a9be1e2b0f111736c00f3d24f6b1e210a063c73a9ba427`  
		Last Modified: Thu, 07 Nov 2024 03:03:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:000c06345544d8d7bbfaf0fd91b79ab35d5e72a9c2c306aef602740e943c7625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 KB (234121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd510e313fcbdb1d3a56cb807a2ca9b5d77a90ecc478e864b4ff4d92d4eec0`

```dockerfile
```

-	Layers:
	-	`sha256:dc971b4639c42a9543352ad156c4d3c1d003f92060effc5d6813d321a70e09c7`  
		Last Modified: Thu, 07 Nov 2024 03:03:18 GMT  
		Size: 208.2 KB (208178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d2dcd4f633710e764ac13b821361c25496c600fea9d1fdaf4861efa9a1af4fb`  
		Last Modified: Thu, 07 Nov 2024 03:03:17 GMT  
		Size: 25.9 KB (25943 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:4942d5fb29765353d457c7f09b089b72559591d5c0c227696f88d8610d683920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76703545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d4a7287488e47ef768d8076e4853b83aafccfabc5d563cecd0a79090e4012e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4e1cbd4051c86d195b2fb96cfc17e7a43cdeb3b02d9c627067475b5a4d1cdd`  
		Last Modified: Thu, 07 Nov 2024 03:05:08 GMT  
		Size: 291.9 KB (291897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899e076c675a549e2d1bc5d05ac9fc56f919b55bb9ec6d441d414eb5acb3e0b`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 72.9 MB (72949892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d622173296eb148f54cd87d18cae3a2b542c4de2fd4c4c57600f64a3449863a`  
		Last Modified: Thu, 07 Nov 2024 03:05:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:23a240ca3a04c91a9965cac8e3cb4b5e06974c83afffbe5aa8b0380994a39434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 KB (233965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4432081f9660490ead9929014413dd5a2e18a97d8b16e985166abded61b70aa`

```dockerfile
```

-	Layers:
	-	`sha256:8bb831bc8e6205bd940401bbf890fc8ba802296c0bf668bf1ae6014580128032`  
		Last Modified: Thu, 07 Nov 2024 03:05:08 GMT  
		Size: 208.1 KB (208088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce48e29621e523caa500b407187a6eca798bd0f81d30d0d0112de96133892c1`  
		Last Modified: Thu, 07 Nov 2024 03:05:08 GMT  
		Size: 25.9 KB (25877 bytes)  
		MIME: application/vnd.in-toto+json
