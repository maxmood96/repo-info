## `golang:alpine3.19`

```console
$ docker pull golang@sha256:7d4b0437e55190fddfc8fc8b7f0c19078cd6cc21d364acba5c3111bd929086ff
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
$ docker pull golang@sha256:7edfc33a6f97678a998c6e06f880bf9101be201e0d8676457322813d214cafdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77715354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58ccb0aab11502af619aef7373a13f135543fedfe8c99d68fb492e70de7d1ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9cbc5befd0446de6aedd42588e72e3b348c70a6a0d7dbfeeb84c47aaf7b94b`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 292.9 KB (292872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bff916ab0c126c9d943f0c481a905f402e00f206a89248f257ef90beaabbd8`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 74.0 MB (74003284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee74b40ef3be5c6f39d735777fd39d5cc87139f13a924f7590e7b039a7cec33`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:3aab3eacf28c1dbb27adf5180d12c536a7182389b2915ba3c18bc22aa78d2091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 KB (234005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ba9d4f0a18fc07fbab42fff86b5bd5ab3f5d3300a7440422e72c701113e442`

```dockerfile
```

-	Layers:
	-	`sha256:15d6e8919802360dba2f656e91c83e35461507dcf61a5e0130ec046f5b2d13ad`  
		Last Modified: Thu, 05 Sep 2024 22:02:56 GMT  
		Size: 209.4 KB (209382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3df4a124bc953cf945b6b3ff8aae66ffa53581d9b07287dfad2bf0867d702d0`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v6

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

### `golang:alpine3.19` - unknown; unknown

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

### `golang:alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:82ed9e6e3c7ee28a662c55014935e48cb722dff523b49dbaef70d07d2c945093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75347927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d5528573d21da6ae909296df88f92191e5a35a1b2d879aef3815f517218eb4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
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
	-	`sha256:bcc6363114f7204e8b9cd3cb47febe5a3082ffb85a82d8c47efb0021f3f9323f`  
		Last Modified: Wed, 14 Aug 2024 01:59:55 GMT  
		Size: 72.1 MB (72127549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3c8e53e9e25a628bdd57fcdda9b37b858a68c15a8988fe55e001ef772f16a9`  
		Last Modified: Wed, 14 Aug 2024 02:02:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:badc57f785391fad43560eb5262100582ca19ac89c831502ad17dd219f592080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 KB (234101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a45dc90cc80cf4093258530e48071542242a59935bf2e6efd9344b9b287ee8`

```dockerfile
```

-	Layers:
	-	`sha256:10cc6f9b668ebae91e564e2192c63b26cb715493c1115ad5f75357f0eb0a5a0b`  
		Last Modified: Wed, 14 Aug 2024 02:02:01 GMT  
		Size: 209.4 KB (209382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1192e7edd49fcf4afe72d9768cb91d0caa53c00888c2d8b25be6cd0d87a896ee`  
		Last Modified: Wed, 14 Aug 2024 02:02:01 GMT  
		Size: 24.7 KB (24719 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm64 variant v8

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

### `golang:alpine3.19` - unknown; unknown

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

### `golang:alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:0ed73b26546eef616da7b95ca4b6d8c9c02c41d446559ee57b9aa87ff3cc4c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75402469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942e4f82e3a52ebfa0781544cf61657645ff529b09bbe59a74c41f0855286796`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
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
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca6ee94cd6c6d373d19e32470d561234f489f1b4d0614cc71e602a68def5ea`  
		Last Modified: Thu, 05 Sep 2024 22:03:04 GMT  
		Size: 293.5 KB (293525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5944571d35e19fa81ca655e6b7753cdb3e37418aa683e0c2a9c169e5d7256`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 71.9 MB (71856183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0770194f3f1a0bdddd9a20a26ec187fc06c7e4db8b34b72002e3bb71f6dbc028`  
		Last Modified: Thu, 05 Sep 2024 22:03:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:5ce165c530a2714977cb7700f8148b59e7e52251acc5bd92c8cff11b669915e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 KB (233909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b28e0bf3076f8d9c0d521f93047da43b5c81a2d8383c769b907538643d386`

```dockerfile
```

-	Layers:
	-	`sha256:81088d7cc5cc50d0d1f449b14c736930fb6b7a172046d81278ad59cc87c89503`  
		Last Modified: Thu, 05 Sep 2024 22:03:06 GMT  
		Size: 209.3 KB (209321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad8a23eaeedd173688feec882cab20fc30dfa88704659dba8595cf2eb56989e`  
		Last Modified: Thu, 05 Sep 2024 22:03:06 GMT  
		Size: 24.6 KB (24588 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; ppc64le

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

### `golang:alpine3.19` - unknown; unknown

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

### `golang:alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:9c7985e5cf58ffca94a132064ea7b4d345bdbffd69c8210635fae8ce1f33ca7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76446503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3293a57faf95cf7ee370bc95c745dd6329f07f7d59c150443d4804ea04ee33`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 17:10:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cf2c1678de6d6936d5e5683d1b785d3f634b44d1cd3d466afe45e4b047ec5f`  
		Last Modified: Tue, 13 Aug 2024 23:12:27 GMT  
		Size: 294.1 KB (294059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d766dfa346f9569deddaa862bfcc6c453c61295fa0688cff4cf096f917447678`  
		Last Modified: Tue, 13 Aug 2024 23:07:38 GMT  
		Size: 72.9 MB (72899210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c70dc7f4834f8ef2f0eafcedb9574a2d1b4d8a916acf9ab5a2825755be645b`  
		Last Modified: Tue, 13 Aug 2024 23:12:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:2bfa85dce556907850743c25913e43edc989f83b5f8e4a2e8ed80ca27d3e734d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 KB (232051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7276978928810e7a52541d549e9c49579f7e93e3229b594f54d7a5fea4d467`

```dockerfile
```

-	Layers:
	-	`sha256:dd02decf899a63812c940487a6efd4ea6a2c3a06dcef8163c5892df8934fade4`  
		Last Modified: Tue, 13 Aug 2024 23:12:27 GMT  
		Size: 207.4 KB (207428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5624544c3a7bcf94f3c46574b062f175e5d8b69515e9ca6e98bc5cf0f57bfa7`  
		Last Modified: Tue, 13 Aug 2024 23:12:27 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json
