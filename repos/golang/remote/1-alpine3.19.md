## `golang:1-alpine3.19`

```console
$ docker pull golang@sha256:2d8e38684dfcf578bde2ea87846c18ab0b273b3de19f6bc302f3af956f549a5c
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

### `golang:1-alpine3.19` - linux; amd64

```console
$ docker pull golang@sha256:fe7e4b58f544d87e61b7cfbe6b1268c32e7b319554cd4328044056a420228e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77716019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910bfff0c5e9f93f97c33358a92816b1508cb19754dc0aa232dcfc75637193e4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22f92c154a38d6ec5066257144442237050dd3794790d49e9565d0a2e1e8890`  
		Last Modified: Fri, 06 Sep 2024 23:19:49 GMT  
		Size: 292.9 KB (292873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bff916ab0c126c9d943f0c481a905f402e00f206a89248f257ef90beaabbd8`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 74.0 MB (74003284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63332a23cee0acb3a2370582060faa8e29068fedf52e246024229fa97d91cc5f`  
		Last Modified: Fri, 06 Sep 2024 23:19:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:a6afa91a55d374ca6b7f083361abdf3fd0bc3ecdab276a9a6e89f08fe1af5e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 KB (234005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bcab590244888e52b2f64201aa2e540cfb47c8b6becb43396d7b3620ac80da`

```dockerfile
```

-	Layers:
	-	`sha256:9f582dfce01a1ad6223fa7e60b2d4b4b909e1dcac73b40a4bdb68fa4f1253da3`  
		Last Modified: Fri, 06 Sep 2024 23:19:50 GMT  
		Size: 209.4 KB (209382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b2cacc7855a9b59e3f987a58dfdc861da44638b3c8d214c931a1646c47b2d5`  
		Last Modified: Fri, 06 Sep 2024 23:19:49 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v6

```console
$ docker pull golang@sha256:bdbefd7ff09d3db273434735f4bd5c99aa3f4ecf4d6f3930eb880cb2b5da3851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75611564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9966b9a1190c0b271b4a5a7fc2c6cbcc50d569791ef4cf078330ec6296b90ab1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0d71f533508426c6991b0b2245e565c1e13a518fff1317af8d93dd6ee5f611`  
		Last Modified: Tue, 06 Aug 2024 23:54:49 GMT  
		Size: 294.3 KB (294288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4760cff10c149b56676c77cd8760221949ab26672a37406e0c3c20879d3fb9ee`  
		Last Modified: Thu, 05 Sep 2024 22:04:17 GMT  
		Size: 72.1 MB (72141445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b8dc9bb54fe077a3bca999474610bdcd6d7953c1dabe5720d598f2e452d35`  
		Last Modified: Thu, 05 Sep 2024 22:04:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:3bbecc3f5d2ce9ff174beb14904ddb91611e273e565ff0fea0f38edaa3194fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f70a1af49960495da8fe62027872acc6fc94f322e9b03266fe98f57e0231bd`

```dockerfile
```

-	Layers:
	-	`sha256:48759ca26e7088d0dc02617207d7b579b2d1af53fd7fafee4cc3897690e1e427`  
		Last Modified: Thu, 05 Sep 2024 22:04:56 GMT  
		Size: 24.5 KB (24499 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:1ca5295743994cadd46ce5cfe9a00acf862fc88b27ead7b2cadd5f9ffe1ce6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75361834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62284e4c867d903e60f26ca00746a48bf827302019e2eb0697f88d06a7792e9f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1950afc2f829e53e58315dd6c28c1e3f9f2b37bada0367ebfa908a36fc329379`  
		Last Modified: Wed, 07 Aug 2024 00:11:07 GMT  
		Size: 293.1 KB (293116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfeb4cb216a5c9d7c74247031f4f727e785d2b0477ebee2ffd136b94b292ead`  
		Last Modified: Fri, 06 Sep 2024 05:24:37 GMT  
		Size: 72.1 MB (72141455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30288b7aaf2044f89abcdbd28121fad4343167dec4c5875a41a3cf1c0ac92328`  
		Last Modified: Fri, 06 Sep 2024 05:27:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:b0e9ed5c9e86fbc2df17385fc7723bd350ca0e0c5140c84ecd6162506b68e2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 KB (234099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54631957b30a6bd3525995bbe25e1649cc153376177a2dea22a273fecad99a5e`

```dockerfile
```

-	Layers:
	-	`sha256:6d2785533cc7529cb13f1f008ae40ca3caf42401af243ccb84e1228e5d9dd208`  
		Last Modified: Fri, 06 Sep 2024 05:27:04 GMT  
		Size: 209.4 KB (209382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e2c22793d400098c7abef5f970305fd9ba939fe78f68cfa08554815193cfa9`  
		Last Modified: Fri, 06 Sep 2024 05:27:04 GMT  
		Size: 24.7 KB (24717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:623803092649288a62ab07347e57e734de6318d2ef7091021f6d4f89449b6665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74279272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc07527df3d9a09630e85515213fa15d35b1309d0bd43326645d05f7856e3cf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dffc9261ed9d2a2cb09dc545c85c340ec5a591a7aaa30a09409757951dc8ba`  
		Last Modified: Tue, 13 Aug 2024 21:38:21 GMT  
		Size: 296.0 KB (296030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355a3cac949bed5cda9c62103ceb0f004727cedcd2a17d7c9836aea1a452fda`  
		Last Modified: Thu, 05 Sep 2024 22:09:14 GMT  
		Size: 70.6 MB (70624628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc2580f7e94f15c645a23825e9fe56739e6dc9b3ea46af6092763ce248b400`  
		Last Modified: Thu, 05 Sep 2024 22:11:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:98e0b5b5c99f9ba1fcfb7b908de2bfd88d46f0e0dbbc939d136817315dfd58dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 KB (234361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d1014f628ccd45cc2c3e08c0c7ceb72dfbd78fe386e9f6ad0d901210046300`

```dockerfile
```

-	Layers:
	-	`sha256:1905ac844ec4afd9301d6807185000fe6cb2616ec77b873fe9856de394548bcb`  
		Last Modified: Thu, 05 Sep 2024 22:11:01 GMT  
		Size: 209.4 KB (209438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74e8060701692de68165cabf8f55f39de39bce0b0e6f34d04fdb6603387b2b9`  
		Last Modified: Thu, 05 Sep 2024 22:11:01 GMT  
		Size: 24.9 KB (24923 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:978164f0d4677d73132d5e21b21bcd9c808a40576354ffeb0cee8861b11ecf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75403470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66723ce8386ced569545d45fe0093728c061d69f07eac3d91ae652162e4e267e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae53dd26de8791eb313599f287861bba82c3ca87f7189373c1ffcb3d28f457c2`  
		Last Modified: Fri, 06 Sep 2024 23:19:56 GMT  
		Size: 293.5 KB (293525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5944571d35e19fa81ca655e6b7753cdb3e37418aa683e0c2a9c169e5d7256`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 71.9 MB (71856183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11fe2c11968321303ed904dcad8156ae332111e414ec5c944b0f7e5781b27e5`  
		Last Modified: Fri, 06 Sep 2024 23:19:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:75da82c6e0bfa0545710ac9166078f61e72c2a11b0587c84b0d6b87368300075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 KB (233911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836d75bdbc3f5bb00d89934d0d8502c1b886e2389057f5704db15bb946fda5af`

```dockerfile
```

-	Layers:
	-	`sha256:25f8fdca5d6d171c1cf3676681e89e6435e900d99054bf43fb05fb14abba73e2`  
		Last Modified: Fri, 06 Sep 2024 23:19:56 GMT  
		Size: 209.3 KB (209321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cccb26a1feec4bf95825e6b2e6a421d9c7d714a9f0cb9505db38cee4c86a499f`  
		Last Modified: Fri, 06 Sep 2024 23:19:56 GMT  
		Size: 24.6 KB (24590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; ppc64le

```console
$ docker pull golang@sha256:306bd597724034014c9289f030ceeb534d8826903bf7649bff046bffd70f14b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74458686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64494330c597d396f65d582e0be17ce9abbad048e2bd04946d50024e5dbfff0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452955a585ac1340f3fc3da244da7ea405b7180ed6f7b0c184fc94a54378b88f`  
		Last Modified: Wed, 14 Aug 2024 00:15:59 GMT  
		Size: 296.4 KB (296443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e5b8a4bec9158fc0bc52aa7bb2055ac421fd36de9ea98898a7188751ff7da1`  
		Last Modified: Thu, 05 Sep 2024 23:28:18 GMT  
		Size: 70.8 MB (70798979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9296d95e0486834905597bdcded05d8630ec1758e095620a7ebebd7e593bc0`  
		Last Modified: Thu, 05 Sep 2024 23:31:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:39cf4c4d450ccb84513204476cf1c418213d5e3b44a51dc864d108cd654e8aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 KB (232163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f4c85194d9fa5f7d9907f86e87e56b442fb9560f90381a6b42e91ee10f02cc`

```dockerfile
```

-	Layers:
	-	`sha256:3a37c437d8651567e320af6c317b2a47f53879e1c43411f2818a7d65dbccee52`  
		Last Modified: Thu, 05 Sep 2024 23:31:09 GMT  
		Size: 207.5 KB (207498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38aedc95603034684c792eb7a8cd0c640bbcd30217d02e12d3338155fc064973`  
		Last Modified: Thu, 05 Sep 2024 23:31:09 GMT  
		Size: 24.7 KB (24665 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:3febd9cd754794e3fdf09cba0dad42b0aa9674265f1cb95668bebb78fcfcbe07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76467337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc96e169cedb4d4e91d5793a3d5cf99bf9054df495a36ace1984a47e73d4ead`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a9a770e2560be5a2440fbd95db5dd7b8326027b6417c76f7ba8dbad71a6421`  
		Last Modified: Fri, 06 Sep 2024 03:39:33 GMT  
		Size: 294.1 KB (294064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492964f2ae9970b6023102de0a48c54b43149da01ab6bb1b356e5cf44a9f6145`  
		Last Modified: Fri, 06 Sep 2024 03:36:46 GMT  
		Size: 72.9 MB (72920040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9667164e0622b1403bce09365f0fff31f11f84e27d8ec38f59c9783389ab28ab`  
		Last Modified: Fri, 06 Sep 2024 03:39:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:20292ef0aa9e27dfbe5d7becd0f323a41baeb5466ec1f047b7bcc2b741e428a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 KB (232051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85d0f1b4308fc71ed2f926615fc0b388fa38b44a857735c19d11fe5bfa48376`

```dockerfile
```

-	Layers:
	-	`sha256:276a2005c7ad186736ff089cdeb5efd979cf76603ff54a0156c58c352f20c87c`  
		Last Modified: Fri, 06 Sep 2024 03:39:33 GMT  
		Size: 207.4 KB (207428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fe286f7e73a29b36346c7fe30e842efb11886aa2e0f151dea0bdda77dcbfa7`  
		Last Modified: Fri, 06 Sep 2024 03:39:33 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json
