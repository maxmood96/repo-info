## `golang:1-alpine3.20`

```console
$ docker pull golang@sha256:ff45d877acb9408879d7d5c0a1aa002f97865496627e7c68c353469bea8ca957
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

### `golang:1-alpine3.20` - linux; amd64

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

### `golang:1-alpine3.20` - unknown; unknown

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

### `golang:1-alpine3.20` - linux; arm variant v6

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

### `golang:1-alpine3.20` - unknown; unknown

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

### `golang:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:524255606d746af71c63ea153a61d28f13a04a0031be0c5aab0427286744f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71104372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505d47b3e7ceb07d1fc3a5244200b122f08795161e218bc69ae34abc120f0102`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1dc8ae002023cf0a7266e02dc08ad7072c292c31e81a16d773ffc91b6aa297`  
		Last Modified: Wed, 03 Jul 2024 02:24:41 GMT  
		Size: 292.5 KB (292467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1377363fadc0bb3eb9a3cd846c096d02c646b0f4af9bef4893106284c049e37`  
		Last Modified: Wed, 03 Jul 2024 02:23:25 GMT  
		Size: 67.7 MB (67716891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af347af85856efbdab23806d3a2fda0de737dcb81504aa880293b165c8bdb38`  
		Last Modified: Wed, 03 Jul 2024 02:24:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e460ff65df76135625b5126cd9e2a631b83a40ff47535012d255e05356570802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594788eff578191b0f88e00a079e7b0fcef3acfd269e5efc3ce31430c63a9b69`

```dockerfile
```

-	Layers:
	-	`sha256:73e41a65fc8ffbbdb9411b732ff1a0e1989cc0323fb825744ab5680e3bc8ab0c`  
		Last Modified: Wed, 03 Jul 2024 02:24:41 GMT  
		Size: 25.8 KB (25752 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d6d72990ed8400b547c91e25b14d97712f4eb9d0c899ed8aed05feed668d1f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70656649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96a5189625045a52a0b26f2513c7deaf5d23da92b522eca0ee8f9a5a37d7a3b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763d8310d87528dad44d0fd3ad17e81221c0c207c455a029f9a94de450eebb7b`  
		Last Modified: Wed, 03 Jul 2024 01:42:57 GMT  
		Size: 295.5 KB (295464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad54470edeaca3376e9010d6ee8ae76847ce9900d3bfcdf32fc98cfd6fc2fa26`  
		Last Modified: Wed, 03 Jul 2024 01:41:58 GMT  
		Size: 66.3 MB (66272226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b1003f5882a5d5a535645e21145ae456e8c0f232071a98b6a80e6e671ef8ee`  
		Last Modified: Wed, 03 Jul 2024 01:42:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e2b397f26936052b9fa1137a4b06b1ff3867452f763ff85c520727645a692993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24238f1a737c25f49d97454133bcef310049ffb34a12c39cd0f84cbe3ab5544c`

```dockerfile
```

-	Layers:
	-	`sha256:645d1ebe4c9575794f076f88ed260f4a6722293cdf5998321bdbc7a523a281ff`  
		Last Modified: Wed, 03 Jul 2024 01:42:57 GMT  
		Size: 26.0 KB (25972 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; 386

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

### `golang:1-alpine3.20` - unknown; unknown

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

### `golang:1-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:6b82c24065125ca7401041d684f81386da9e93927ce8ee4653139aab1fa10af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70317177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859d5d454a48fe0232710a084e61da5fc8ad0e0573a63872e6b9825119a13c8c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3141cc44a06fa9dfe1043039bedefb2cd2aa916e27b73c9ef646142752a5003f`  
		Last Modified: Wed, 03 Jul 2024 09:53:39 GMT  
		Size: 295.9 KB (295886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442a44a1d407a5a3d1cba7a7a9b8820f3afe463e19c35ae36202ab5abc57af4`  
		Last Modified: Wed, 03 Jul 2024 09:51:53 GMT  
		Size: 66.4 MB (66449434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72a7dab85399d9a82f7970684a4d27605f837da7571b61bacd41007d2da948a`  
		Last Modified: Wed, 03 Jul 2024 09:53:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:b4c920440d082cae23ac45917cc97b900fc379c7fc3dbf4be5e98a173dc77cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706c54cbfa9df363d31009202b62d73f1625e64e49b7fd42e0d6341fcc75306b`

```dockerfile
```

-	Layers:
	-	`sha256:19d097550614799fd995128d4e5a6b61b32be0b7b2af51a6d6fc824f51338707`  
		Last Modified: Wed, 03 Jul 2024 09:53:39 GMT  
		Size: 25.7 KB (25690 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:27229884e3bf2952597bdeb77b6e1be3116a63273e851126ae47ff14a68f0262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70567475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bc84d930a346ea8949c7348c5b7b2b1e4af662cc8daeb0609f4d2e0f5dcc95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fabd91b6a1a591759f176be6e8c4ddf7d6c5b79c5fffe72fa34ed233e62f93`  
		Last Modified: Wed, 03 Jul 2024 01:24:08 GMT  
		Size: 293.2 KB (293186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39589efb4f4523cf902577d9136ea8d30bac98adf4bfb817724f0f6dbfa86c`  
		Last Modified: Wed, 03 Jul 2024 01:24:18 GMT  
		Size: 66.9 MB (66903096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fd487051268d12d3ee5ad597726cedd9dee83912d9ab8ecb8b6669ade27ff2`  
		Last Modified: Wed, 03 Jul 2024 01:24:08 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:f503a8c23c6c3b15bd1320cbe5dca475d14b23ca8ecbec74113eddef4697c611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3094dc0a4648f63dc2ac54e8ae6207d53b3b7666165078c27b994272c1d4d4d`

```dockerfile
```

-	Layers:
	-	`sha256:c1d4d571be3d01288d5e9e90831874025bc0f46da288c332b46998209cf984df`  
		Last Modified: Wed, 03 Jul 2024 01:24:08 GMT  
		Size: 25.7 KB (25690 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:a8d78b603053adf3573b93a3bc0c3accb7a7f6237d41a6470107be4a17ba7ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72166996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599959bd786df3e5f7bcbb8be90e38ba59d3721524aa604e62ec345f1a0c2ba4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6075f580ff9155257f851e1279c2fef823c1d43c42d2bf92f41b459ec8db60`  
		Last Modified: Wed, 03 Jul 2024 01:09:31 GMT  
		Size: 293.4 KB (293409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36325bf1498477d36098ce5907eb7a794a2e7eb1ff088a91163f8cf4d9ca6b9`  
		Last Modified: Wed, 03 Jul 2024 01:08:00 GMT  
		Size: 68.4 MB (68411572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6f6007c9329045de5e9eb34e33d4910d207bf4c542c6d21724a0ac4001d3c`  
		Last Modified: Wed, 03 Jul 2024 01:09:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a45b0d6afef570994fde79725e70960dbf5a7c93e554fc10d3a803e0e217f219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96665eaea0c708295004fb7ae7ea25ddb05f34cce44dc9a86394dc2f380396c`

```dockerfile
```

-	Layers:
	-	`sha256:4f033662b72b3e7b40666538cd6eaa6d15e61cf2e82105279168d523ae1f7bf8`  
		Last Modified: Wed, 03 Jul 2024 01:09:31 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json
