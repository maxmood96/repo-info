## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:58bd102a6205691eabd9400b05e574c2877f7d40264701c9e32bbd2c2797ac8b
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

### `golang:tip-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:d815bc81a5926ad3471fa3b9e362c931f9b3ef351e46f250ef9f7bff664b1d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130778766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f05bea29679db6470c8bfa98e3cea38684124c6e255d653e3da862c5d299489`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa607b32ac589b60d6af83dfa20a5de75f0fb5269f08b1e2a465aa786ec062b4`  
		Last Modified: Mon, 21 Apr 2025 22:37:13 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25d4babeaf90344f4555f59166692dee6d066349b1a2f5cb41fc36591cc0aa6`  
		Last Modified: Mon, 21 Apr 2025 22:37:14 GMT  
		Size: 126.9 MB (126857323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fab576db461ea6787924435f447246df7c16462cf65a5e355c162fda1dbc97`  
		Last Modified: Mon, 21 Apr 2025 22:37:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:d5cae24eaf612063f698da634147d1a1db309ae434b4b02f4d0a02298d43efe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229997e284741bee1f8f5f399ca9eccd74d1e2e0c5f0e270982235605b379085`

```dockerfile
```

-	Layers:
	-	`sha256:df462bec3dbbeab5b162c9cb3c208273876369ad441f274cd1de871bbec9617b`  
		Last Modified: Mon, 21 Apr 2025 22:37:14 GMT  
		Size: 205.4 KB (205443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b9959f09b8e97637f209ab2163300d4fd858a5c5c473ce9101effb1b969f60`  
		Last Modified: Mon, 21 Apr 2025 22:37:13 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:4a19b9b05b3c36450a44c10d233c03b7cee53cf75bf21e5d6e361276bbefc289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125910479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1ef4867b5dc62d372f179d244eb906a4186bdc6d0d91e414a62027f55e0eae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7bf435709d1c27794da4aa58bbf1c4a90e82ff2338f06023036bd847c51bc`  
		Last Modified: Mon, 21 Apr 2025 22:36:52 GMT  
		Size: 122.2 MB (122241957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d98676a1b77c2a167ad95c1cbd1590c5f811a487b9595186ea12fb098c934`  
		Last Modified: Mon, 21 Apr 2025 22:40:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ac994b03c86e27d3e03437329b0d8892476246f0501676dadb9e41eb073e6e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063dc954634e76d813b0cce506b4b938fb638253c8d4ec3d34f51827084b0896`

```dockerfile
```

-	Layers:
	-	`sha256:fe62bfe035e13539b40b4917bce7fc97781fb429e6c302616722fe7ca2e3b276`  
		Last Modified: Mon, 21 Apr 2025 22:40:18 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:9ccfd4d426f0b8d38b94a4bc2d1f12af32852bcddfc416494af20dc43df751aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125290727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b924e41e550a4f06c1f00257a992f2501f3aff9785245ee9efe87970f4cf26`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5cc54485761ae69a05b08a84359a87e39a46bace5d6d721b8ddc84655c07c3`  
		Last Modified: Mon, 21 Apr 2025 23:32:56 GMT  
		Size: 121.9 MB (121899846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2327ddfdf22ce10a950d6a5974b671eabec3fcd9cfad814f766fbb507db30454`  
		Last Modified: Mon, 21 Apr 2025 23:42:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a63dd4ac4b3deae2886482c651453fb560eb02ba5632fff9fc2a24eb73f57ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b880b57f1263ea226443989f612902c26e6ae90298e5a6d19931387690053c`

```dockerfile
```

-	Layers:
	-	`sha256:648e985fd6daa8ad353cfb64d4a4dfbba0f7cbb77fda8100cfbc18a2b4e813f5`  
		Last Modified: Mon, 21 Apr 2025 23:42:22 GMT  
		Size: 205.4 KB (205423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becb0bacf6783415e60a42a2d027b776d1c2a464d37cdaa8ad1886b5d7820939`  
		Last Modified: Mon, 21 Apr 2025 23:42:22 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3dd97423c19ecc40c386bdd578844bab6a57116660165ff0b033a663a0b605fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123938150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41026e28a4f111dc4f74f5c962011d2bb6bfefd25726fb4f2ffce5230f7be09`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d91181a4474d3822cc4cabd1e8df2eed7942133a31b6fe7528c1a3639a00d`  
		Last Modified: Mon, 14 Apr 2025 21:56:34 GMT  
		Size: 297.5 KB (297478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49c3c4d9fc32722fbee95cae35a84bb5c2c18fa016fa934c1de17d28a4bfa33`  
		Last Modified: Mon, 21 Apr 2025 23:29:01 GMT  
		Size: 119.5 MB (119549349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15adaae393645f0e21cb5feea476dbf6922744c163d0a1acef55981edc15456`  
		Last Modified: Mon, 21 Apr 2025 23:35:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a5fc79f79056aeccbfe790229c3d3d0b38ffaba13ea6b78e62062e898271249c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 KB (230122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ddebad16a5124ed9fcf0b3ad9d72727e64f197854e3c92293474c0610a258e`

```dockerfile
```

-	Layers:
	-	`sha256:16316307f17ad838f0632ee26c0af375e128ce4a8ad05df0a2030ffc7a72b46e`  
		Last Modified: Mon, 21 Apr 2025 23:35:11 GMT  
		Size: 205.5 KB (205475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d75123e81c9ee4e93fa293c90bdb67b12377f1fca31798ff7f79db60813ba22`  
		Last Modified: Mon, 21 Apr 2025 23:35:11 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:2f0f86c5de3766058996f77e0483ede868ae3359cebdea59f1bcf4443d7305e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128810440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea3522ecd544c7b54251ea93d8ce6ccefc43ef8c261c520a85db02e29ea5f5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da19f81f95234be2f436440204e905609ce287f59a8f5bf2cd302f3da51b8c13`  
		Last Modified: Mon, 21 Apr 2025 22:37:49 GMT  
		Size: 295.1 KB (295137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22385500e9d61ec2b239f5d3bd81241409c720a3ebb2a4cf2d458346f64bcc50`  
		Last Modified: Mon, 21 Apr 2025 22:37:44 GMT  
		Size: 125.0 MB (125043477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72177e65800fe60930d540caa24cf09db08868e358e6b00d6aeaf76223acb6bd`  
		Last Modified: Mon, 21 Apr 2025 22:37:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:8301cb5c0cfc6611c7338b124e85e52696c0e172b59fc6b5b839b45f43867bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c5445586a18dac89bb926c568c242c76601e39c29039c01a1c52652670382d`

```dockerfile
```

-	Layers:
	-	`sha256:f8ef6bd4e11dcd4015b0cb0a7d99be48896226940139fbadff9d6627421dc5c5`  
		Last Modified: Mon, 21 Apr 2025 22:37:49 GMT  
		Size: 205.4 KB (205388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1112779d67d9225cb6d9c7322a7d483b17486fc0e10d7fc4b027985ec9a204b`  
		Last Modified: Mon, 21 Apr 2025 22:37:48 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:d2461ec4f6efba09b27ccd7188bf9d8cb0dc123f8dad9e15f81aaff3b104f19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125558232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb298789bfc42f0bc579232cfde1bc56bdae07ab23d89aeb693f8a97ab84c4a2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5950c2617b2e37b28d36382b32bdc610566f7587eaecf172653230b9278424e`  
		Last Modified: Mon, 14 Apr 2025 21:58:56 GMT  
		Size: 297.9 KB (297899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb73d167b954c764acdc0a85e569cafdf41ff90d8b4ea6c273076608592e7a`  
		Last Modified: Mon, 21 Apr 2025 23:41:09 GMT  
		Size: 121.7 MB (121684495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09faaa8b33ee6bc435e97789bce3e148c658022bd1040480da9805dd823ccb`  
		Last Modified: Mon, 21 Apr 2025 23:48:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:2cfa4efd8d0ab073b4eebcf63abd578abe010f06381d5d18ff962ed6a87a0b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 KB (228112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9f1fc4dbdba164c49267ddf207b0cc5a7c378119106fac5ce5260708ce90a1`

```dockerfile
```

-	Layers:
	-	`sha256:aa46ba67d8dc4c99bb2568294503cbf37ca6da344b84eea8759de1e641c3cbc1`  
		Last Modified: Mon, 21 Apr 2025 23:48:20 GMT  
		Size: 203.6 KB (203554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3129891835ea8bc5991baac9d4bb7c91d2f8b3c9ca9d7496085d58c680d452`  
		Last Modified: Mon, 21 Apr 2025 23:48:19 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:db07878f4da6209130b3f4e87f0d321f44433af738534e0cd484ebf8a05913b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125707381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb5576084690850b0e23172bb3e7a6f3c5d39f38bb3994c583969b010a8f9c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb12bf697d577c42f53f652ba0fb4c4093c94ce6986095953e539f07ea9b28f`  
		Last Modified: Tue, 22 Apr 2025 00:14:55 GMT  
		Size: 122.0 MB (122038546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4e481f4d39b148cbfee82157b624667c704179fc22ee5d81ffab8d666be2d9`  
		Last Modified: Tue, 22 Apr 2025 00:52:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:fa579489812307ca0ddf69976299c3589f0e5a50e03abe628bc1f921ffd955b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 KB (228108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b9316e257af9230b0b6604d71c5828dbbaf1909913b801deb18e0f3b36aff2`

```dockerfile
```

-	Layers:
	-	`sha256:e30e50012223f2363d51f28474054af21031a5f47031a9657547b42d78f4e74b`  
		Last Modified: Tue, 22 Apr 2025 00:52:45 GMT  
		Size: 203.6 KB (203550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81483f02d569793e591c6c1a22ccfad8da418c3d5e7c1039b2aa5f0eb31ac972`  
		Last Modified: Tue, 22 Apr 2025 00:52:45 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:8b0fe3be9678116be759962d4f9f3adf01e9b2ae190963190347fceefe8d8d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127881767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c3991de26ed1bee3bd19b00e35f37052e195c13c6e2e906210454cf087257a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e7fca1d9a730d1f433c30e90db2ee0f57358064bb42fafd714109fc27562`  
		Last Modified: Mon, 14 Apr 2025 21:59:00 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221a3257b37adc23c0f99fc0f36d93743cedb18eca41076488eabc753a5b4701`  
		Last Modified: Mon, 21 Apr 2025 23:08:47 GMT  
		Size: 124.1 MB (124121776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb97367f566a355092e3fb023ad7e5ef50ae46a016b8212f1bb5f13311c7d5f`  
		Last Modified: Mon, 21 Apr 2025 23:14:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ce6352146b95a3e3743a0293c7c28c49e5391f43ff2d06857202c5d48abc1a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53ed0822e2a75f443b556ae154a44ca9496cdc39444dfb15c0faade54cb55a`

```dockerfile
```

-	Layers:
	-	`sha256:30afe0672460baab23084a4e512b2bf04bf1716fb88710e3a40f6b9758c66485`  
		Last Modified: Mon, 21 Apr 2025 23:14:33 GMT  
		Size: 203.5 KB (203492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4dd153cef8eb34d04cc0097921aa79f1d39b664a7be088a80518de2e91bff78`  
		Last Modified: Mon, 21 Apr 2025 23:14:33 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json
