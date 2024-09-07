## `golang:1-alpine3.19`

```console
$ docker pull golang@sha256:5aca55f186227f4792484cc22a1d94a455eb4a85f9a54c41742b039d5cc7022a
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
$ docker pull golang@sha256:e410a57b3e02b922472ea4ad48ba18a1baab48ccbac518f0b1a2c462ec3deb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75612276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780c9e7fc4fe74fda32adaead67021ecb5a6a0995ba2d8905de1c8147a870d77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a189aaa8881b35f02064df0565f1c166dd7085fb308b5414059d2a5ec1777`  
		Last Modified: Sat, 07 Sep 2024 02:31:12 GMT  
		Size: 294.3 KB (294282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4760cff10c149b56676c77cd8760221949ab26672a37406e0c3c20879d3fb9ee`  
		Last Modified: Thu, 05 Sep 2024 22:04:17 GMT  
		Size: 72.1 MB (72141445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1399e83abae489053f3a77b7be2c64692b17572bbb116ed3820be56da0d16`  
		Last Modified: Sat, 07 Sep 2024 02:31:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:213d5ec778417b808d0cab91e81a3db7b8352082779a26c3f3e304c470127916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5263ae8dd8c6d1766803cd6a67e8231b2a078d4ea6620a726a2c39f65c1398`

```dockerfile
```

-	Layers:
	-	`sha256:07aaf6a1897e48d5b634aef3f58d2efb06a5f2caa34b5b8f06e10938045830ef`  
		Last Modified: Sat, 07 Sep 2024 02:31:11 GMT  
		Size: 24.5 KB (24500 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:2f75817b7ab719957a0c82074f4cf76c889328129c23d809df79219f02c51c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75362396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4fe0d372f6ba06280200df1b632daf72371bdb2873a0d4057eed693fd92dd9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
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
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9ebd6f2ffaff5b11ed965eda965a2876a4fe296d1e665173ebec7499446da`  
		Last Modified: Sat, 07 Sep 2024 02:44:18 GMT  
		Size: 293.1 KB (293118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfeb4cb216a5c9d7c74247031f4f727e785d2b0477ebee2ffd136b94b292ead`  
		Last Modified: Fri, 06 Sep 2024 05:24:37 GMT  
		Size: 72.1 MB (72141455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d083353c2a7a7bbd88aafa233c5c948fa5ecf1f6f7c401d5c59b275f5bc75`  
		Last Modified: Sat, 07 Sep 2024 02:44:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:0ad7c5ebdcb7077a95f065087c9daa63ca9870d4836b07c01790f3d72dbddd0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 KB (234101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d54b3de189cdfaf7ecbe62ba4b14ef57347e7f9d3f274988a60266f15d9568`

```dockerfile
```

-	Layers:
	-	`sha256:594ff64b091b1797bf9877ba34afde71e4eeeb42f4bd14494a406ef3bf3a1840`  
		Last Modified: Sat, 07 Sep 2024 02:44:18 GMT  
		Size: 209.4 KB (209382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:095c951ebb99e369e4f045af13f419ccfdaf09a7da9e757c38006ee393f2272d`  
		Last Modified: Sat, 07 Sep 2024 02:44:18 GMT  
		Size: 24.7 KB (24719 bytes)  
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
$ docker pull golang@sha256:adfdc425db72a8aab74e5cdb2c3148ccdaa57d4d7266d31aca328f04b0b9f3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76467619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf2c5df4ec9d3c532d09fffa011164abbaa6150645259771abfa9187c367e13`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
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
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894081f2f13d315f0b572cbcb8498f72c609da816bf17dac27e2707e6a7e0461`  
		Last Modified: Sat, 07 Sep 2024 02:37:30 GMT  
		Size: 294.1 KB (294064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492964f2ae9970b6023102de0a48c54b43149da01ab6bb1b356e5cf44a9f6145`  
		Last Modified: Fri, 06 Sep 2024 03:36:46 GMT  
		Size: 72.9 MB (72920040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd105750729c1bc21aec1902614a08ad04e72e6d27d69d26c4f8375f526f000`  
		Last Modified: Sat, 07 Sep 2024 02:37:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:275670cf7c6a4d0afdff696370f17cec9cdedad19263efa1beb778578836d0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 KB (232051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef9210f2d969f5660d73c941bb57aacc7dae0b95cf3143b5eca4a10633a5d44`

```dockerfile
```

-	Layers:
	-	`sha256:ae69bc03727b5844d34f9c6abf316d7b79739ecec96ae73a23e6c3bbc7f67afa`  
		Last Modified: Sat, 07 Sep 2024 02:37:30 GMT  
		Size: 207.4 KB (207428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7225a48d9fe8e9e4f928655f44fc6c8b2969812401bfd573234ed9651b383c94`  
		Last Modified: Sat, 07 Sep 2024 02:37:30 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json
