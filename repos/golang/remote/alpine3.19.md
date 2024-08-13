## `golang:alpine3.19`

```console
$ docker pull golang@sha256:c525e799d673016d0a79fe5cccd450c634cc3a7b9c4524ed37836fac84910684
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
$ docker pull golang@sha256:d51a8d9d94def6eb87d5851d78ed86c8b348b99d1c6982c8fe70d2addaa90c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77677377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7513740d8b3ba5c66e89161f65db0399ad689ddd519c8c5276f520107bb080a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e92e90b52ca74e66f6bcebbbaa64fd50ce66bf777515a6c40b30283f87b003`  
		Last Modified: Tue, 13 Aug 2024 20:02:17 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b14fb4020d7e427735797bf663a02a5a028e40fae0f8993ed5dfe75f15417a`  
		Last Modified: Tue, 13 Aug 2024 20:02:18 GMT  
		Size: 74.0 MB (73965318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84e58cc09b473fa1718c4215f940fc6d4ecc0cb8c3c56fb7c1a0e96df31370e`  
		Last Modified: Tue, 13 Aug 2024 20:02:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:d197cb1336ad77c14fced01b6dff1a4336f22fefcf5bbbdb20d84b22a0fd0b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 KB (234005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd59ec6c0eeac6d494d7f3394a50f02f4bdfe7c30a0d121b64e1e81cbaf546a`

```dockerfile
```

-	Layers:
	-	`sha256:1d3c8f1e5668136ca6e433770b365f59dc66cfd1c7d7acc91d6ceb803301111e`  
		Last Modified: Tue, 13 Aug 2024 20:02:17 GMT  
		Size: 209.4 KB (209382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34404130b9bb24377ef7e6d66e042e1d5ea849ea9534529d1f63fc6a448578b7`  
		Last Modified: Tue, 13 Aug 2024 20:02:17 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v6

```console
$ docker pull golang@sha256:bb3200fa69a1d9eb26ade025b8ea9ceaeb95a4c8885458db627db42412d7b497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75597526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef161f0c57ef1b94cddeabacf2ddcb96ae0f63ecd3d7436ff3cd5ec3633c063`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
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
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0d71f533508426c6991b0b2245e565c1e13a518fff1317af8d93dd6ee5f611`  
		Last Modified: Tue, 06 Aug 2024 23:54:49 GMT  
		Size: 294.3 KB (294288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2264fd077e48bbe464da15268c0dc5d530f2daf4be4ca5923887f3657309c3`  
		Last Modified: Tue, 13 Aug 2024 20:04:23 GMT  
		Size: 72.1 MB (72127409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc83f96ec631b78654dcccbd898168cd89607a439471e6e56c5ca5d9ecb00e`  
		Last Modified: Tue, 13 Aug 2024 20:04:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:7fef030d3767347c68477c262a8c6735dc9ac6c0e04e835eec199294369b3447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec33e4fc32796092487bb1a13818ac654f2b701781d741a61de123cf43f9764`

```dockerfile
```

-	Layers:
	-	`sha256:c135b56a1a53c91e03350134dad303a71eacd9c4ebb1a94e0f1fd3f14ed2e2aa`  
		Last Modified: Tue, 13 Aug 2024 20:04:59 GMT  
		Size: 24.5 KB (24500 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:e28a896a8109a9a45cf0e644db472a7113070ed8565e58d856d618f7915d1ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70949372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a286a058f1d13bf72228e3ab6701965e39d28abdeb9b23f593618aba83c77391`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
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
	-	`sha256:38353948ef7c4a85c3e42510197b5f321621d39f3094140f1496e3ba11d3156a`  
		Last Modified: Wed, 07 Aug 2024 00:08:57 GMT  
		Size: 67.7 MB (67728993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6ca7029f6f0df99d5328d30e172f46ea8d861a8039f4825193b66f74f65386`  
		Last Modified: Wed, 07 Aug 2024 00:11:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:316d49e6add9e62b98387d666fc8e4da39a2aab8d65590a615aa590e1055e58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 KB (233698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966536213b6785555f5143245834840eb07421f6294adc86f94a3dc990c0c7a`

```dockerfile
```

-	Layers:
	-	`sha256:64bcb91c18ad4257240ea339daae9b25ccb4910500b991088376cf3b63aaac6b`  
		Last Modified: Wed, 07 Aug 2024 00:11:07 GMT  
		Size: 209.0 KB (208979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9f9911737764fc6b8c4a3470637ab1d14a54b6cdd322d5825d9ec1aa345cd6`  
		Last Modified: Wed, 07 Aug 2024 00:11:07 GMT  
		Size: 24.7 KB (24719 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1cef3003be0889e1aa4a4dd92f8cbe0008c583d05d05792611e3e3ae5dbe35da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74262562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca78a888da7febff161cacafd2fe2f3ca284ac995d85d0284dcc1074d36d3270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
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
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dffc9261ed9d2a2cb09dc545c85c340ec5a591a7aaa30a09409757951dc8ba`  
		Last Modified: Tue, 13 Aug 2024 21:38:21 GMT  
		Size: 296.0 KB (296030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f9ed64c24993ada6c5d1b00ea7fbf5720c6cc30c9ae14d18134989fa7a08a7`  
		Last Modified: Tue, 13 Aug 2024 21:36:27 GMT  
		Size: 70.6 MB (70607916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c43c77b3e81dfb1787b65a43775d74348a3863d0823bd6742f21b0c65648`  
		Last Modified: Tue, 13 Aug 2024 21:38:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:28108c577ce9cf2a4424c305c4d19a1251505c3cc7ca0b47fb1fffb93fde4aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 KB (234361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffb45f143d5fe4096cde28e1a57fb639859672369633be34aa3cdb5ef596e72`

```dockerfile
```

-	Layers:
	-	`sha256:c11451d1edb67ccd20c32567d74c082fd51ef911ab2497f8adb47b2815b4f7ac`  
		Last Modified: Tue, 13 Aug 2024 21:38:21 GMT  
		Size: 209.4 KB (209438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39c02398314842e9ad8bcf24101555e8aead0decca55aa683f3b065cf455efc0`  
		Last Modified: Tue, 13 Aug 2024 21:38:21 GMT  
		Size: 24.9 KB (24923 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:e7ba08f009c46b8e072b8cbdca6dc2d4bde10af56088d937cc5f67562940cbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75402928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f814e9b73775eab8f8e26a356b30e2e2b00ec21e5090be9d41c3fcc632edc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
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
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc822ff3e2b3ae7ff4d1494675ffb30fd49599a0d0716af6f6403d0ae4a10af8`  
		Last Modified: Tue, 13 Aug 2024 20:02:20 GMT  
		Size: 293.5 KB (293535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a02128519d4902024135fc03b12145f389fd4b2b393eb6499f6f10486bc83`  
		Last Modified: Tue, 13 Aug 2024 20:02:22 GMT  
		Size: 71.9 MB (71856633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e84d305cf290f96adf21e151692fa5339d21b1027807b8f28c395b51dac1269`  
		Last Modified: Tue, 13 Aug 2024 20:02:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:40aa27ab24b4868bf176c0679fe9a37848261b307d7b959c2c53acc583c43267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 KB (233911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865173f386e4a644d2462b0e6730c776141d9b8df9e02a55e74138ab4ce4d57b`

```dockerfile
```

-	Layers:
	-	`sha256:cda356db64f670815fe4ce15356fe9ca0f25a6ccab340f36790fc169a51b85a8`  
		Last Modified: Tue, 13 Aug 2024 20:02:20 GMT  
		Size: 209.3 KB (209321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ffb74c662e7ae19f945e52588ed0c20ad7894b5e9d6826e5cac4d23fbe037`  
		Last Modified: Tue, 13 Aug 2024 20:02:20 GMT  
		Size: 24.6 KB (24590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; ppc64le

```console
$ docker pull golang@sha256:8f67b2046aaa8f11450635dc703ab81fabec50721124de0fc572551f29999f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70113589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6ed1d0b6ff5a80c4ef9a7b03552862e9e3993e47217f8844adfa0319416491`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed040c7b9ce3ee358f66fe341301724e17033ba8d8dd7353608dec4431a2845`  
		Last Modified: Tue, 06 Aug 2024 23:00:21 GMT  
		Size: 296.4 KB (296443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa907a73ecb9721e6fd07eeff45b3daafd73705b1b26a4ab050075d2da72289`  
		Last Modified: Tue, 06 Aug 2024 22:57:05 GMT  
		Size: 66.5 MB (66453881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9d7ee1bfd554b9bed480a68d980154fa59690db7e06ac829256467fd424a98`  
		Last Modified: Tue, 06 Aug 2024 23:00:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:42e981ab7d3141a02ae427757f5dbd601749353e5e6f625939e4a3f45d71d21f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 KB (231756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8910e081c6ecb034ca873bab6bc654beff6b413c640c84033dbe65e1b97bf04c`

```dockerfile
```

-	Layers:
	-	`sha256:817d92123458cdc31efa6496a0fbd992c8cc751adbd72696bd62bbea60afdfeb`  
		Last Modified: Tue, 06 Aug 2024 23:00:21 GMT  
		Size: 207.1 KB (207091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1973d90408135eaf527c24155b7173d140b0e38a751af2a5e0d99cdd215efe34`  
		Last Modified: Tue, 06 Aug 2024 23:00:21 GMT  
		Size: 24.7 KB (24665 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:14346b464855e710ecd99d4710c3ace7987de3456ac7fb4276bff62106e868bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71968253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe3cf92529fb10d9b7234235ac3399ef38ecd4c1576b0872ab21e15d976effd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c676daa7141401fe10daea55af78a668c289e5e595520134befbe84fe344a7c`  
		Last Modified: Wed, 07 Aug 2024 02:10:49 GMT  
		Size: 294.1 KB (294051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4f522c886389638258537d7ed45e62dbad030e5ed340cd291df30569fc9288`  
		Last Modified: Wed, 07 Aug 2024 01:54:06 GMT  
		Size: 68.4 MB (68420968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0164e9dcf30164e1df11867429250a81e26d17269e35fc35a373e43810b894d`  
		Last Modified: Wed, 07 Aug 2024 02:10:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:802c2f7b4126c70dc34833f093e71133da26d7b377343ec3b71ab4c8b0b31aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 KB (231646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56132397f8a30b6a1d183468d2a9030ce42402934e88c2441f729ef454b9971`

```dockerfile
```

-	Layers:
	-	`sha256:f79efcc2d7f1907e682dcd28c0ae07b65a887b8b9ca5f9fa4914495d5fdb4360`  
		Last Modified: Wed, 07 Aug 2024 02:10:49 GMT  
		Size: 207.0 KB (207023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e1533e3504331bf91ec5813cc77fc0aa97f7233a4ad0e5e07106e7cb7945d2`  
		Last Modified: Wed, 07 Aug 2024 02:10:49 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json
