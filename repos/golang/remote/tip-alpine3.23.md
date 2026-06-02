## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:01e45a1b511a09e5ed9237ea36c0040b317d1b1bd02bcaa9aa6ba1d606653c50
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
$ docker pull golang@sha256:161a21e6816f428c12a732ee690ede2e1a68cbc88fa7e8bbe63a0722e85e4885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106156752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b24b8c1787be1ea313afa25d5097ad075a6a7f80bae48748b87b858930a7fcc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:40:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:42:40 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05866a9b2a6326a082673e8d2ceced47d92be7e4350a5c561de3a0f30611369e`  
		Last Modified: Tue, 02 Jun 2026 16:42:56 GMT  
		Size: 290.2 KB (290245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f29da6194068cf9bcb9d5261ce3db2ba9613e69bf068059cae42650df5c10`  
		Last Modified: Tue, 02 Jun 2026 16:41:24 GMT  
		Size: 102.0 MB (102002162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11508a08d38cacdd5e414581e0f2c38b76455eb65ac16a8ea2d8168f8790002e`  
		Last Modified: Tue, 02 Jun 2026 16:42:56 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:3ea5f6b60954c94543f52dc32e691e1b3580ae8774f489a27b1a9c46842610ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f94d9ab075a5a8b95e05a115a60b9df1ca29577d58fb6d8d242d9658cb0c04`

```dockerfile
```

-	Layers:
	-	`sha256:adf2ffea3c2290642550d9f577f3886529889185554365d4690b75be14c2e41b`  
		Last Modified: Tue, 02 Jun 2026 16:42:56 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1befd5213031c4beacf0b3ef0d6cc3537ced8c5662843f533fe0e3b6b751cb86`  
		Last Modified: Tue, 02 Jun 2026 16:42:56 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:f5430f5d70a8f210397181230cf09a1500bb35017a10258ce976720f9fb02467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101880929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f94271751e4f64a256c4d1049afe10b6e91cb04d2d17a082341a66a69621aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:38:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:41:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:41:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:41:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29587a82f4a289fd6eadd17a8d35ac10943e0866cf0c34e042b7d5c91bc51cb5`  
		Last Modified: Tue, 02 Jun 2026 16:42:07 GMT  
		Size: 291.0 KB (291029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e28476efd8da64969ee963c59bc7bbb65ceb1b7045e417b1e645826aca392a`  
		Last Modified: Tue, 02 Jun 2026 16:42:09 GMT  
		Size: 98.0 MB (98017879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7d286fc8ad2b0ce9700f32b3370cbe759b0ce37e8cb9d0574f186ed0aadb86`  
		Last Modified: Tue, 02 Jun 2026 16:42:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:6e0046b0dbc96347f2594a1b6011d57b94301b12c4bfcd9bc22bbd536db092c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7351270608bc971e5122f07cc8394bae588f58bd29f7bf902e9f800816071a6`

```dockerfile
```

-	Layers:
	-	`sha256:5d18334b5bc3957014574236132f0b4ef2d5ef26ceaf01cb71d92d6dfb1dcb02`  
		Last Modified: Tue, 02 Jun 2026 16:42:07 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:00736c77fb6419349bd19531c5ae7876f67dfe5e778f5f36ce108d6db60dfaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101288505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cc0169d7a76e0008d7f9517387296282f9285beceab1f32961c7eba5f19d5a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:40:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:43:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:43:54 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:43:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:43:54 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:43:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:43:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94db899b72774af0ca6b01de24c6c100ac18fa3f3d3233155cc3d019ebc76a13`  
		Last Modified: Tue, 02 Jun 2026 16:44:13 GMT  
		Size: 290.2 KB (290168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c820ebe5b5536b95e87912c5dc1f2663a3e9f184b88c7a174fffa610cef8238c`  
		Last Modified: Tue, 02 Jun 2026 16:42:07 GMT  
		Size: 97.7 MB (97715056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755639e0540d2ed8d33c4bb2a44ebbcc47ddb70b26184b2fe45671ad256e5a72`  
		Last Modified: Tue, 02 Jun 2026 16:44:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:cd34f1d89e1f97f35ef53b923e8e45f17f01458cd30ff070c6207699f9df7a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c74e160012f65f16dfa93b955e6904865145feec9abbbb7981011dcada8bcc7`

```dockerfile
```

-	Layers:
	-	`sha256:27fdd561653fb730a3b82f725867e1756fefebb721791bf0a78c9fdefdef9ec0`  
		Last Modified: Tue, 02 Jun 2026 16:44:13 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f369c3de8ff73bee602e1ea46952043a541c4b13a21b024d292bf44228e48a8`  
		Last Modified: Tue, 02 Jun 2026 16:44:13 GMT  
		Size: 25.2 KB (25222 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:daf8bd1905848f37471d1fd1925fd58dcb8ccb01dedacb9ef0681379a68595f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100927472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2ca7cdf29b216262462ba089d38f9de593368c3d3757efc000adff8344edc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:39:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:50 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:41:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:41:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e1c082f681aa001579c15e55cde564f44047532b5e1dbb9a62112c42353cb9`  
		Last Modified: Tue, 02 Jun 2026 16:42:09 GMT  
		Size: 292.9 KB (292863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ffb09d61853e3fb3628a4cb3b2d395b59e27aec015f8f1626a8b2ce9bb2f2`  
		Last Modified: Tue, 02 Jun 2026 16:41:30 GMT  
		Size: 96.4 MB (96434582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8c412e3ef04074163afb296c5bad0a1163d3fdacb0a378037f61e56064e27a`  
		Last Modified: Tue, 02 Jun 2026 16:42:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:f8bb39bcd2cfb91924f7426ff814319e8d46b756102584c8f6ad2b071cf494b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ead0bce694b34e9161c88d198ae4261724eea3d54cb751060965555b14867`

```dockerfile
```

-	Layers:
	-	`sha256:8043d6dc7da5160b94e976eeb323567f960f19b940ebbc2abd030ed33e797d8b`  
		Last Modified: Tue, 02 Jun 2026 16:42:09 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9968a51de9f8365b6df180bcd8ad38e8df53964b6b31a8c1acba1380c220130`  
		Last Modified: Tue, 02 Jun 2026 16:42:09 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:5621367107b4165ae34ff7e8909a40271659796467739ede48460f2ce9f80e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103750776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6b86b22c2cd4a26b28942af6a5b38f7290f8e1c3bed4ad39596af87458213`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:40:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:43:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:43:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:43:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:43:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:43:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73576facc532e9c9a9f8bf892bd8883025811e88417c13f960d02fb55ac9c78f`  
		Last Modified: Tue, 02 Jun 2026 16:43:19 GMT  
		Size: 290.6 KB (290644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f630b89f59dc6a4b85d53c6ab2696f0b52ea5d937a0bd9344e6c06fc5883a6`  
		Last Modified: Tue, 02 Jun 2026 16:42:33 GMT  
		Size: 99.8 MB (99769529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fbcc47cf8a89b87e0aed2662c57836177d72b0f5c7d714b63fe8262a42312c`  
		Last Modified: Tue, 02 Jun 2026 16:43:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:bce03ddb311e86ed420c9d6ebd374d1c716d039cf6781bcc533b23d5a2d2a8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cde1851d61fd7a009681cc5e5d71bdd638f245d4fdb0362d1fdf73d006296b2`

```dockerfile
```

-	Layers:
	-	`sha256:db0135aec36f69c85af7a035dfbb4ee08aa5f7de9178209ed17544e2813dc148`  
		Last Modified: Tue, 02 Jun 2026 16:43:19 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0c21682a775a7f6a912b9f1c22605f92594a24db4217ac2f17f7355f402d0b`  
		Last Modified: Tue, 02 Jun 2026 16:43:19 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:79ffb95538073be198e3de5af33dcba1ce7d1b3416de5ba4afe54e739f926536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102511572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a15e02dac5c0684f45260590b5b0fe56b49704768858b5c5ea3282aa533c086`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:50 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:47:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:47:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a76d2265265ac98a5752cfbf5ed880207c013050351547f0c225cf8c995ca0`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 98.4 MB (98387092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16457bf361a3ee87c6b040957b6f70f261ed1cda1dcfdb420d68e8f4510ec17c`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:a6293b2b219f6fd5b1b7709f0c3f8cbe1ff39ed899647023439d470b38fa859f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c57725b6a929211962c7795029cde7bba357ddccc87031e40f10596a54a4d85`

```dockerfile
```

-	Layers:
	-	`sha256:0a345d913c0f6dfd799e7c2a13965fe782cfea341b71e12233e2ba3e8d5eaa1e`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5e6f4698ee4d48878769d33b784cf3a08443ddc5c9a4e2fa7a15d732fd882c`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:69a240971c4af022e04c74d5f58ab219f6f4c8013cc206f813a855eeeb399962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103040797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746d2353e4b01331a0fb0031923f7e9769bfa00bace397de4ca71d67e71a9378`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 28 May 2026 11:35:46 GMT
ENV GOTOOLCHAIN=local
# Thu, 28 May 2026 11:35:46 GMT
ENV GOPATH=/go
# Thu, 28 May 2026 11:35:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 11:35:46 GMT
COPY /target/ / # buildkit
# Thu, 28 May 2026 20:30:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 28 May 2026 20:30:15 GMT
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
	-	`sha256:f9ba57acf5ba3d18b7eb9e4286139141d4a6480c2e9b8f4fd881334e86e5e1a9`  
		Last Modified: Thu, 28 May 2026 11:39:26 GMT  
		Size: 99.2 MB (99162424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb20ac87d29f824de6fab9598c6fd5a0880f18db7211c8ee556298a9b236cd3`  
		Last Modified: Thu, 28 May 2026 20:31:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:463b26775137a5917dafeb660baddbabe96106d659567ff79398571b8a8ce691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6d87bfc343670d667eca4af5fe3e7b7ebc505ce1ede15156db441c0990237`

```dockerfile
```

-	Layers:
	-	`sha256:ff62d029da4797ae66f0d7030539fb521319f66e71244d19ef54e9e918286f6e`  
		Last Modified: Thu, 28 May 2026 20:31:31 GMT  
		Size: 193.0 KB (193043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92687eaa665ac6af13a90170c45d4a67616df7433e2948227c051f671b8ef4fc`  
		Last Modified: Thu, 28 May 2026 20:31:31 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:488b070e623f6857f658d41ae0bcf36a5bc4550acb2801a2c14916ff225fa589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104471502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e283ec8e162a7458fc22f703a1a747543f089e86c6ef1b44b442b1dbf7651b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:41:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:57 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:57 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca767cc33ca0e2036ed1bd1b9a5ecdd963a3598306969640db0e92025a10887`  
		Last Modified: Tue, 02 Jun 2026 16:42:28 GMT  
		Size: 100.5 MB (100453651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640cefbc230cca6ce1e699b6f066a0ce3ce18296f9bdf22d36a86823e240dbc3`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:84a7ee03e028b86025e1c9827d4bb323847db40c8c20a4c8f318af896f54efe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91489d918162f6fcc0aa8a085c9f26b6b670fd28f680e2e629aeb4852a45ace`

```dockerfile
```

-	Layers:
	-	`sha256:ef0cdbed5d693509dbf06f0b5aae4adc4a9508ce4144f1fbde4dbea737e5b7d5`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 193.7 KB (193745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61e5a72761acb3e21514ce110bdb096dcac7d5b24cbb11663df5261872584ff4`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 24.9 KB (24923 bytes)  
		MIME: application/vnd.in-toto+json
