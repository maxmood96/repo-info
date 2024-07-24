## `golang:alpine3.20`

```console
$ docker pull golang@sha256:0d3653dd6f35159ec6e3d10263a42372f6f194c3dea0b35235d72aabde86486e
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
$ docker pull golang@sha256:6b6f39cf7399e3042f040ee7c66402aaa7801be5fe07c1bb298a10e5f45cea2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73266022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f132aac134a24dc4a7c5fb004654a3118de7d28e71e2b46629abd85fd6a56a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a3c6a2fc325ddd7b489e14e23a849659b705bad1f9a25f92c709c493bd8520`  
		Last Modified: Mon, 22 Jul 2024 23:04:03 GMT  
		Size: 290.9 KB (290877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a2f51ff3dde07bfa1ce35b5597b2d97295e64a461d98e696feda7b25a6dc5f`  
		Last Modified: Tue, 02 Jul 2024 22:06:15 GMT  
		Size: 69.4 MB (69352095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce758d8279c9c9b9ef1179dc238ebf3c0158d63c21c8129e20dc54f901ed8614`  
		Last Modified: Mon, 22 Jul 2024 23:04:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:1ca24c607871f94e8838b0abf634a933157a0a288cb365d3841405eb3ca6dd14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1263c7f73c0f4b2a7fdcddf40a6a375de2efa57944767710d03989709caa3656`

```dockerfile
```

-	Layers:
	-	`sha256:35096ffd473b53aff07c6c99c88789dc5e6c9210315687a596ea409046df8a44`  
		Last Modified: Mon, 22 Jul 2024 23:04:03 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:962f85ed3a637eaf6f73120c69f15e4f6393be2de526b14647a8c3164323572c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71373957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d01657232fe7fd83a63eaed87b4c1bcea91a061a021116ad99ff2c22424c42e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
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
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50535c4d10f19285cd6d86b0385c339419a1927b1b5c8159c7be4368bf8dd01c`  
		Last Modified: Tue, 23 Jul 2024 02:51:40 GMT  
		Size: 291.8 KB (291773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a528a178c88ba9b89a4047689ee438ae3a530ce2004fe5bcf7bd618341780f`  
		Last Modified: Tue, 02 Jul 2024 22:22:24 GMT  
		Size: 67.7 MB (67716837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274f5f95256a4bab090b300da41d88496f586ec909ecb3a5e41d75f5ffae2153`  
		Last Modified: Tue, 23 Jul 2024 02:52:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:8d56b32faf178f4247b8ef8e28fd64afd201cf9b84950c4cd8f987b18aaf0e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7085577a19e704332778cbc18397f6871760f51b4b7a09e541a1c6669d2fa4`

```dockerfile
```

-	Layers:
	-	`sha256:299fba99c85a3e3bb56d90b5355dcd4407eeccb9a8b15dfee593cc2db1e23090`  
		Last Modified: Tue, 23 Jul 2024 02:52:58 GMT  
		Size: 25.8 KB (25752 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:ff7f6f4bffab719651f2a010440b51c1ef8c05dd2e415f18ac83051b2b8dd746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71102958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d300fbf816dbf96c62a06a15ddd128c3d5604db7e57601bc118d70d3b4fc8a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
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
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45cb03661eab28e36c526dd0349b4ec3a2d6dc7abcb5d2d95deb63ecfd5e53d`  
		Last Modified: Tue, 23 Jul 2024 17:14:59 GMT  
		Size: 291.0 KB (290951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1377363fadc0bb3eb9a3cd846c096d02c646b0f4af9bef4893106284c049e37`  
		Last Modified: Wed, 03 Jul 2024 02:23:25 GMT  
		Size: 67.7 MB (67716891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e524d4ce955251ca753c6a6cf897d0b289114753ebe1c84d9228bbc8fd6e67`  
		Last Modified: Tue, 23 Jul 2024 17:14:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:7d9d1192e22b3ce16524cbe25dc532c57b5a2f2920dcb3980619a9070a3f8ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921b7e1bf521637ac3327876bf1f122bfda2753a3b1bd20e7c1c6753ab0b2e0b`

```dockerfile
```

-	Layers:
	-	`sha256:3e024191981bcdb78cae613138c4e743e859375900d6c8a75605e7b72d618210`  
		Last Modified: Tue, 23 Jul 2024 17:14:59 GMT  
		Size: 25.8 KB (25751 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7ac4fe4954e9da52d5a6b316c32b3201e7a1bd34d8439de1f0183fc08ced2366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70652818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d19f7090dce0c11c1ae9fb817409f16b9383b975763ea547f067104fff72e6b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39127310aef1912eb0a4e5274d9f758ebcf254c6087d4bfd758a5919135ad95f`  
		Last Modified: Tue, 23 Jul 2024 17:34:21 GMT  
		Size: 293.5 KB (293501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad54470edeaca3376e9010d6ee8ae76847ce9900d3bfcdf32fc98cfd6fc2fa26`  
		Last Modified: Wed, 03 Jul 2024 01:41:58 GMT  
		Size: 66.3 MB (66272226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd18ca2ee67547d327804f9220d1af2f8512a5de0ae83d77f86405178736580e`  
		Last Modified: Tue, 23 Jul 2024 17:34:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:bb49d789cb29865c92c8d58a315ef5b252cd4a279575eda44a633b2707a53bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86be383d594181bbfb8b49447e090f542704df7758fcbfddbac1112ed7a7cd1b`

```dockerfile
```

-	Layers:
	-	`sha256:497f725deea67b9d21207891be7875d0c60ca095889a29d8ca43324e46943af5`  
		Last Modified: Tue, 23 Jul 2024 17:34:21 GMT  
		Size: 26.0 KB (25972 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:44aa1724b760eb9383d4cb6ca3d49de010055b4e5aec3a87998722067d2d460d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71100944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c340faf6f2286377f61473070e6849d2cc4f59d0ec90490104b1a0048f54329`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
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
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88ff8087e34707c247e7094f926cf1fd84b7a42e8b97f519f5236459c3805b`  
		Last Modified: Mon, 22 Jul 2024 22:09:07 GMT  
		Size: 291.4 KB (291359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b75921c461b2ae6d1ff16df768b5e8ff34e9b73cf9704174903aa4e8c76f79`  
		Last Modified: Tue, 02 Jul 2024 22:06:19 GMT  
		Size: 67.3 MB (67341356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124b36319e261606ed21756e8a70445c6f3b1dcbcd66c1650915ac7ed9540685`  
		Last Modified: Mon, 22 Jul 2024 22:09:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:b0c3f60b8b0a45c2502262bdef5640d6fb79922067749e9f3a05334057ec19d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0fca1d3133bb282b1eb117a061e89ae37878fae8845d5aa7c14dbbe482f395`

```dockerfile
```

-	Layers:
	-	`sha256:7c2ffff52885e925a43d1e28f2d03dd12a0ffd9a844d7d52532a158a1e9d2a27`  
		Last Modified: Mon, 22 Jul 2024 22:09:07 GMT  
		Size: 25.6 KB (25571 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:c5db744df471194c74a8f667d11b40ea1189669873b28b2f7b5c20e5445f8753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70315158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2491c26e14d851ff3750f02ac0d65d05a53399d68704e92b943cc5516758f25f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
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
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bce206c4b8f573240cbd89b6737334874c007d5902fff34a156f3b1138964c`  
		Last Modified: Tue, 23 Jul 2024 16:35:19 GMT  
		Size: 294.0 KB (294012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442a44a1d407a5a3d1cba7a7a9b8820f3afe463e19c35ae36202ab5abc57af4`  
		Last Modified: Wed, 03 Jul 2024 09:51:53 GMT  
		Size: 66.4 MB (66449434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c1a6bb0ad5c5cd638648f6c79bdc682969743af194508973632710ee32c15`  
		Last Modified: Tue, 23 Jul 2024 16:35:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:10ed3e759eafe2b9815cb958b75bfdca7bffef53b12395be70ac66a68328329a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4843878196c76fa9b47402e34397b26315bf166c8748d0371a550421a4aefd92`

```dockerfile
```

-	Layers:
	-	`sha256:6cc556330569f7b5d9e9c64fe5ac7567dfd6a6d8e508e153cad12e7472d5ee66`  
		Last Modified: Tue, 23 Jul 2024 16:35:19 GMT  
		Size: 25.7 KB (25689 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:a6067818458cfc78479aa2780a426865abd390284a103ad1edb50a6b6dbfe123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70565603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993e7402f7cc74e1c69562b2636038097a6738c0dd862a1faa1af001180d971c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
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
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4b8bd895aa555cf42dbd4f6d0d401c883af31e3e18cf44270e14e66e941d5d`  
		Last Modified: Tue, 23 Jul 2024 18:52:23 GMT  
		Size: 291.7 KB (291677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39589efb4f4523cf902577d9136ea8d30bac98adf4bfb817724f0f6dbfa86c`  
		Last Modified: Wed, 03 Jul 2024 01:24:18 GMT  
		Size: 66.9 MB (66903096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45d282d20518df48b8076038c3ac8af2ead6ff738e7e605fb5be9e986f2b0a2`  
		Last Modified: Tue, 23 Jul 2024 18:56:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:de163b83c8dae16d557abca7ce346de04275482a14490f2a9b6d7c94135e53d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49e42f4208c77b31ace6fa19a34942b11df02dca1df1a55b8b70c3dea0caa93`

```dockerfile
```

-	Layers:
	-	`sha256:b0594791b73c1f55cb7a09382cac1da9dc48de32325564e19f5187b93a656874`  
		Last Modified: Tue, 23 Jul 2024 18:56:07 GMT  
		Size: 25.7 KB (25689 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:ae51438616901b2dec079150e18a7051d0a4196497b83a5dd0d8c91525290a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72164687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c0932a6728a27abc5b77370fbc00bda8c46235098d8935f9300fec06504588`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
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
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dcde3e7a1bfe9254751178a6a5e5c239cd1c93e3f9724ba489ae55c2e9f3c3`  
		Last Modified: Tue, 23 Jul 2024 15:54:45 GMT  
		Size: 291.9 KB (291891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36325bf1498477d36098ce5907eb7a794a2e7eb1ff088a91163f8cf4d9ca6b9`  
		Last Modified: Wed, 03 Jul 2024 01:08:00 GMT  
		Size: 68.4 MB (68411572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785512e0fc23495638787c0f998bba647af4ae4611ae3fbfd088571acd9e7b9`  
		Last Modified: Tue, 23 Jul 2024 15:54:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:8838bcfca5d0d86f830eb4ec4fb5350eaf48985dd8adddfdf57e93d80925a7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6e62e7ca8e7c0a3708882766914393f5cfa2539f62335f7318261ce94774a6`

```dockerfile
```

-	Layers:
	-	`sha256:8e23be6e0fac823c59e98ae39e2488aa65d323e6b863a2b83ec6e0202607ff28`  
		Last Modified: Tue, 23 Jul 2024 15:54:45 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json
