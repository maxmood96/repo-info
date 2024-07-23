## `golang:alpine3.19`

```console
$ docker pull golang@sha256:653cab079ac76c46f5ee0c04f121e95e463f94a003bb10ff62d28de7100ab2ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `golang:alpine3.19` - linux; amd64

```console
$ docker pull golang@sha256:97d28dbc0383657568b9589cc554a6ad14f5384d3b5ec3e236fb11ce5a9c1519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73064144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b43c5fa9b2c80d4ebca865b447f8cce2f81136c0eb102c6716a471b1f13a7ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519806a05888dc39ebd99a930a09d69a4ae1398d85fd7f23efbf4f2f71c1f421`  
		Last Modified: Mon, 22 Jul 2024 23:03:35 GMT  
		Size: 292.9 KB (292851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a2f51ff3dde07bfa1ce35b5597b2d97295e64a461d98e696feda7b25a6dc5f`  
		Last Modified: Tue, 02 Jul 2024 22:06:15 GMT  
		Size: 69.4 MB (69352095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578b0943dae8ebcc69396709b68197bfb8d5cd7cf9c0c73cb255c7c08057051d`  
		Last Modified: Mon, 22 Jul 2024 23:03:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:473c95f6084506a5c84f2756b311fc6784e049bf2ed22f4e013535ece651ba3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ece6f2c9edc18a3037dd21f24291943f0a58bb2632567157f3cd8c3c6235dd`

```dockerfile
```

-	Layers:
	-	`sha256:90f6d3513ccefdfc6752f94c30e00efd67bc58883146ef374b0266945c972755`  
		Last Modified: Mon, 22 Jul 2024 23:03:35 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v6

```console
$ docker pull golang@sha256:30cb25a51533c1f5e9958931ab42abdc9b48a693ec92be9b27a2b716510e7d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71185170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7ccea41931cb9a41789349528494dcf54df0392df81242451b8e259ca037f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ec588bf79b2155502188e08df24aa54ce2d3f88ec6b02137fef7a5bffbb0a`  
		Last Modified: Tue, 02 Jul 2024 22:23:00 GMT  
		Size: 294.3 KB (294268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a528a178c88ba9b89a4047689ee438ae3a530ce2004fe5bcf7bd618341780f`  
		Last Modified: Tue, 02 Jul 2024 22:22:24 GMT  
		Size: 67.7 MB (67716837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576db6498f816d1c99541e08fc65cc273781f07d526cb7244bb11980bf0be73d`  
		Last Modified: Tue, 02 Jul 2024 22:23:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:4ab990c2c89dd8cd250ad71c356d6b8cbbaa6579d19e7b195cb7437fe0c89962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457001db18f26035be1161a81efd4a29e7244971fa9a7613c2b4c48ad60c29f7`

```dockerfile
```

-	Layers:
	-	`sha256:1fef9136f2dbcf46d3d25191c43b483978c00da9a7074fcb92de91cfa22f3479`  
		Last Modified: Tue, 02 Jul 2024 22:23:00 GMT  
		Size: 24.5 KB (24500 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:8adde4bdefb08b40e1d28cfacd38955f90b461982de0f4966fcf673703f743af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70936665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00eb25fededdd616e6d18961f07b33203fba64f116f6f3c9aea7542652e3a267`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:32 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 20 Jun 2024 18:00:32 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16f4b77a55cd40d8a5ba426b20e23a195ef7c7c1814b602173cb9c76147d28e`  
		Last Modified: Wed, 03 Jul 2024 02:25:12 GMT  
		Size: 293.1 KB (293118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1377363fadc0bb3eb9a3cd846c096d02c646b0f4af9bef4893106284c049e37`  
		Last Modified: Wed, 03 Jul 2024 02:23:25 GMT  
		Size: 67.7 MB (67716891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639171b7c9c3ea87ddd251ed473381a78201e38309fde6403f15569a4064f0c`  
		Last Modified: Wed, 03 Jul 2024 02:25:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:210741e08b37638d7a7a078542d5a16487c478fbf21620a8180f2b04454b051e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea86b2027d2a525398af22bba9821a5ac5ab5cd0ff0346dd7b3c233ff631a61`

```dockerfile
```

-	Layers:
	-	`sha256:1f27d0eddc9cf44b14734d257db357dbcd21867da0a47eb064d83386b30f817b`  
		Last Modified: Wed, 03 Jul 2024 02:25:12 GMT  
		Size: 24.5 KB (24500 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:38bfd69d0ee6f995661bb7a23970d75a3d7a8665dce6e4819a74da3ffbdb9543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69925603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1018986456e053e2fd499feb4e06f69a4624a3b1a392cb978396153e645143ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56575cb2eb493f21ef9bc7ac10c7825e5f9d6066265b66998142d9c563c0ebc0`  
		Last Modified: Wed, 03 Jul 2024 01:43:21 GMT  
		Size: 296.0 KB (296018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad54470edeaca3376e9010d6ee8ae76847ce9900d3bfcdf32fc98cfd6fc2fa26`  
		Last Modified: Wed, 03 Jul 2024 01:41:58 GMT  
		Size: 66.3 MB (66272226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03890413a9bf31c1b45bd2107d55ad92d9bce67fb9ff10fd036584e5bb2ae06`  
		Last Modified: Wed, 03 Jul 2024 01:43:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:441002952dc8621fca515cdf4f044409b0626fc430ed216de0dd3e089589b06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ff19730f9e98bcf857171b3594bfab4e3ba2e3ae8e297e870dd2672106a037`

```dockerfile
```

-	Layers:
	-	`sha256:a2e385ca1407c23878c35ffea2c17d2a7dcf0180a2e07b85b5954942ad631a7b`  
		Last Modified: Wed, 03 Jul 2024 01:43:21 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:ef5bb10e9a15201b42e4856ed31d39a670f0f84a5e9a70b534b66954d3473628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70887631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf57c4d324c10effbd0e4c6fd6f4411d92596c016438e3c513bd2da6eef844a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed0a3f78ba323c1aa364124165153452370316fa565475ab1c8696adb3905c9`  
		Last Modified: Mon, 22 Jul 2024 22:09:21 GMT  
		Size: 293.5 KB (293515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b75921c461b2ae6d1ff16df768b5e8ff34e9b73cf9704174903aa4e8c76f79`  
		Last Modified: Tue, 02 Jul 2024 22:06:19 GMT  
		Size: 67.3 MB (67341356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37762c632e24714752cf6cf1cd73a8e2ab9eaa0452a01b6adcb6f12ca037b857`  
		Last Modified: Mon, 22 Jul 2024 22:09:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:c6ef8d3cd82a3c8819b6d613527d41baf266a57c58a78354c2c7d0b212fea87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d82be30c287ca41fca9ea348ea048871e1bfc93f34abedb1eefa0809ad14cda`

```dockerfile
```

-	Layers:
	-	`sha256:387744f125cb21ea554d298d5fc11879f26953922f4032882bbd08b8877d537d`  
		Last Modified: Mon, 22 Jul 2024 22:09:20 GMT  
		Size: 24.4 KB (24371 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; ppc64le

```console
$ docker pull golang@sha256:76a7c0d5eb5cd5e4f49103280710a1c12bbd298960f41184156ce2a39c7bb277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70106661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc3b21c20d7c71a03d3b559dec1e7ce61464d0254f7930f6532c857f008e599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b343aa84f9ba24a37629963bdeb41ef6f8a2d4de21513c2a2a52215ff4d3d2`  
		Last Modified: Wed, 03 Jul 2024 09:54:20 GMT  
		Size: 296.4 KB (296434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442a44a1d407a5a3d1cba7a7a9b8820f3afe463e19c35ae36202ab5abc57af4`  
		Last Modified: Wed, 03 Jul 2024 09:51:53 GMT  
		Size: 66.4 MB (66449434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48db1cb9ff5ad3be3a36b258f8729548a5b122e12716aaa8876e6059645d2a03`  
		Last Modified: Wed, 03 Jul 2024 09:54:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:725c3494a678155c1462da9d47f549d9dab986ce955a32e306540c346bf46f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6973ade054d045257669197aab70feec64b6fbdfc0b852332202e0c91214897`

```dockerfile
```

-	Layers:
	-	`sha256:0e05166670569c0ba0cb6d8c655fe1199692d3e66d5d89c870065e4a98bec1ac`  
		Last Modified: Wed, 03 Jul 2024 09:54:19 GMT  
		Size: 24.4 KB (24446 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:588b9714abf9067997e613f897965bcd8ddc8dfead627ace1fa5754ea0ffbc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71958267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4660fa314103eccb388377ca7ef05de2b4dcc6e4e2e2bf48ce1b556de6a3fa39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920f6af9a26834ceee8a0012313094e167f889ce645972dd1ab62a56d18ac347`  
		Last Modified: Wed, 03 Jul 2024 01:10:14 GMT  
		Size: 294.0 KB (294046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36325bf1498477d36098ce5907eb7a794a2e7eb1ff088a91163f8cf4d9ca6b9`  
		Last Modified: Wed, 03 Jul 2024 01:08:00 GMT  
		Size: 68.4 MB (68411572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab88a6f18e5a276452356bc238d184108c1023492e2100e6bc1ae787149a2c0`  
		Last Modified: Wed, 03 Jul 2024 01:10:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:4ca32ff53b1c4907cccfdff6bd4a37b05a4791a69b09814f39a4c1632ecfb87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f084cbae2957308b9290429233ac8ef1ef40a40c5ce0ac02b8154aa101d9412`

```dockerfile
```

-	Layers:
	-	`sha256:b102969271e520ff614be15a4a30ccde31af734bd6147ac93ecdc902829aae31`  
		Last Modified: Wed, 03 Jul 2024 01:10:13 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json
