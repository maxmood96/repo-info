## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:73436f5d769066122843a65c012389553983636897dd29268d70ad43c820c87d
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:6726b7a10f3e9c75ea4e971540c3420be2d6bcf3d589fb2eed5fe13fd6cfc767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95560521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e517cecafba7d6dbfa8705366ab717528451800549591f6fff147e174d3793a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:07:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:06:55 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:06:55 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:06:55 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:09:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:09:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da30cdc66b14b2a518aafea6a1268bcfa9c0f1ac51c374543d332f79a551a70c`  
		Last Modified: Mon, 03 Nov 2025 18:09:25 GMT  
		Size: 291.1 KB (291126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cdc461d8e5b6378706696b9d7cb2bee286c3be63889d089612a96810cc10`  
		Last Modified: Mon, 03 Nov 2025 18:07:51 GMT  
		Size: 91.6 MB (91626668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738803bbc475b1b8e4accb837d3b5190651961a606c6d7a773338dc39611af9b`  
		Last Modified: Mon, 03 Nov 2025 18:09:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e10aad059411b74ede57c3046feac92b44094dc083a9f994ad8daac0af65578e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1b4fe62375a399664322d69fd8d33d4c3c5ccd19bc568ec44b9d5a02e06138`

```dockerfile
```

-	Layers:
	-	`sha256:fddf3fa66dffaf737a3245ce5accfa9d1f99adc010a65a06c5c33d7de4e94c5b`  
		Last Modified: Mon, 03 Nov 2025 21:24:18 GMT  
		Size: 194.2 KB (194205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:326947698fc65e4ac3c354859b9803502c48506252e240aa0bd428d7af36d126`  
		Last Modified: Mon, 03 Nov 2025 21:24:18 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:f1a146045732a19cfe265793a84ea350d7ebd7138ed8df509d353d9ad7842e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91722459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84ec34116fabbab0e59aa3f7e451873b0adbf44b2e48d5371c0077444ad43cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:05:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:08:16 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:08:16 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:08:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:08:16 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:08:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:08:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0421a378fd37ed2a977524dedbc0bebcdc17aab1407ce2a3dd29646dc002afc`  
		Last Modified: Mon, 03 Nov 2025 18:08:34 GMT  
		Size: 292.2 KB (292241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f518140b1232c759e1bbff002fa828b3b3a5b3d09a55146300b06356a080e134`  
		Last Modified: Mon, 03 Nov 2025 18:08:08 GMT  
		Size: 88.1 MB (88064592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b305cc28ed253c607cdbba397dcea857706905874f65d60df95a22d9b8b8763`  
		Last Modified: Mon, 03 Nov 2025 18:08:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:07f17b789e1d6a01b79018c8f292b66f7682efea7f8490291a1d5f56d1d44244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1908a9153b92812ade87c42513bfdc68117d4823f45d02d12664542d89561a`

```dockerfile
```

-	Layers:
	-	`sha256:2d0a8212d9ecb9fb965490a2dce88d9f5c9b5c6d62c46579d98e2b36510fd97c`  
		Last Modified: Mon, 03 Nov 2025 21:24:22 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:46556659bef7cf78fcb42a66b346a9fd220c59b5e9c091f8ea8d198134b4d237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91196593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ddf9b266d4700d914629fe9f252386a1931c70ba5d98b9afd706117ccca9e6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:07:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:10:26 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:10:26 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:10:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:10:26 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:10:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:10:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eef3b987d568fa01d0f2422eafdf09828faa82e238168ef84b50c3592ecace6`  
		Last Modified: Mon, 03 Nov 2025 18:10:48 GMT  
		Size: 291.1 KB (291145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc3193360041d5ec3fd6b5f23bff516805dac965b3e6d2a23e404f02fefd2e`  
		Last Modified: Mon, 03 Nov 2025 18:10:00 GMT  
		Size: 87.8 MB (87806679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04fa8b7466ae0e4ca778c4e38107d35f2c98868092735ff06f7d99d00c3e2d5`  
		Last Modified: Mon, 03 Nov 2025 18:10:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:4d8609fd7e307cd77fdd0854579f7812332c45b827bf2adea1861316738c3069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f4191a996569716ec5e030c307bc790a89dee8fd241e66f767856b97d26c37`

```dockerfile
```

-	Layers:
	-	`sha256:1da80717a198985efec1dc3f1ad0b6da5af252cefac8adcea53076ea6e1d8e0b`  
		Last Modified: Mon, 03 Nov 2025 21:24:26 GMT  
		Size: 194.2 KB (194209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f461a47080ced4646ae902acf30e953f395380b40411f2bab40e1f6aefc6261`  
		Last Modified: Mon, 03 Nov 2025 21:24:26 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7a6cfdef2f072b02757d1577ae51150c807f1e629cf3e1741ad763c470a17d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91165135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c37a54fd825c6d870fae4f0ae54c971577e583000a72c6ab66a89962144d2e0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:07:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:06:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:06:51 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:06:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:06:51 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:09:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:09:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4ac8965d1115362a09994082cc2cfbc0368a34952a4c79fd1ba6772b3fd5ff`  
		Last Modified: Mon, 03 Nov 2025 18:09:26 GMT  
		Size: 294.1 KB (294056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a31d309655c21bc621f07e8c42b1089ab055b4f9c298c53b0ddf3b945ebd2f`  
		Last Modified: Mon, 03 Nov 2025 18:07:42 GMT  
		Size: 86.9 MB (86878571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9434baee447aeb480650e5bd0ad8500565751920954fa113888b7a1698b84cb`  
		Last Modified: Mon, 03 Nov 2025 18:09:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:934e50c91b11295fe10abb5f40c1031224f96ab774d7d718b76f9a541de06646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29f3723b69d749c60cf460a737a9b0bd7afe595274f9f255d730a1f7e74d861`

```dockerfile
```

-	Layers:
	-	`sha256:12170e9b7d783c84956248e1b279302db3ff1eb61b7f4193ac41d73035adeac4`  
		Last Modified: Mon, 03 Nov 2025 21:24:30 GMT  
		Size: 194.2 KB (194237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b6d1a33c5a6d2f0470df7aeb29e8548e5a44e232697e9c9e48ce8663dc2532`  
		Last Modified: Mon, 03 Nov 2025 21:24:31 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:3de42adef3d0802f4b24dfae1563ed7b24835ef1ef11810f8ed2db5f3c98ed66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93369493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b112548cfdebb770aafea5021842e4c2bf91f439041125337f1a8b650b4e424a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:07:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:09:22 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:09:22 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:09:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:09:22 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:09:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:09:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54d7d1bbc7fb43266fc43bb60c6ffc5815a8df5ba28aad05335f4307dc6e595`  
		Last Modified: Mon, 03 Nov 2025 18:09:44 GMT  
		Size: 291.6 KB (291604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db89236eeebef76fdc6574b93130c4a0c99f66c249e46e945ed95e5d140c9856`  
		Last Modified: Mon, 03 Nov 2025 18:08:37 GMT  
		Size: 89.6 MB (89613027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc4c4aa7b8bc30b65025602e89ae7c80bc81c037e56e05ba849a25a5ddd5a8f`  
		Last Modified: Mon, 03 Nov 2025 18:09:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e9cfc41f8594ba79eb64f4f96a7805bdeb6c56c70fc01918cca73578ba5dba30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1376dd818d7f3f5460f813570ac1976e2966044455ac3e7e95bacb486555704a`

```dockerfile
```

-	Layers:
	-	`sha256:f6a005e371a67faed39d3502a9deb0052db5257850a1949b6aac9f9f3ca09e9c`  
		Last Modified: Mon, 03 Nov 2025 21:24:35 GMT  
		Size: 194.2 KB (194174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a15fb666da765b07503194f581628aa494dbb700d1f33c89fe746c14ad3530d`  
		Last Modified: Mon, 03 Nov 2025 21:24:35 GMT  
		Size: 24.4 KB (24431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:ea98108f5c2e45db822aa27f1dd7c9c933b8764c2ad1c96527b300f4534e1b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92160626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f650ea034977ea9f4c7c74e3c6851db7246c8fba3765b89f0ddaf773e426f8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:21:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:40 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:21:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:21:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157fb47bb8a37b39db37d445bdc0f41d6332fc70e6aca92f0fee08bb53d187e`  
		Last Modified: Mon, 03 Nov 2025 18:22:12 GMT  
		Size: 294.5 KB (294530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11f1fd4cd7eff0746fa6b81e430f63f5332dd96bd03a2e634ca5fc29dcb745`  
		Last Modified: Mon, 03 Nov 2025 18:09:48 GMT  
		Size: 88.3 MB (88291863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5a88f48ef60e8ab017a20aa0069340d5651c61a8b33dcb43628642434d0b4`  
		Last Modified: Mon, 03 Nov 2025 18:22:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e56e0325ced5aec5b3e0fefe2a1e5d6e1cc7f0189ce07b60f40b63c5804230a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adb6dbf59e0d38850dab232934eda0bb27cbdb76e4ee0596ca04bf3420c05d`

```dockerfile
```

-	Layers:
	-	`sha256:682460424bc007ce18e5f21ad23a4155cdc4254210405b84819ce1808d203d8f`  
		Last Modified: Mon, 03 Nov 2025 21:24:39 GMT  
		Size: 192.3 KB (192292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d077bdd1fc5e0bb8faf01a620837422a5d64e09c71f399b33a2f29f3d743c25b`  
		Last Modified: Mon, 03 Nov 2025 21:24:40 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:8e49ec14ceac580fca256fe14be7ef2bece99abdd6823ce73c1de7aa7cdc9928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92439040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250bd55d03a5cd53c6223de415fb30e4a01f181645065b6d895eb4f208a889d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 10 Oct 2025 20:46:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 19:28:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 19:28:57 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 20:46:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 20:46:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611661040751365eafd7f1dfe7a29755674f06b893fdaa0640152a38b160d0dc`  
		Last Modified: Fri, 10 Oct 2025 21:10:14 GMT  
		Size: 291.5 KB (291463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568766c8d70cce8f34aaf3713ad1c1267acad6ccddf02bbbe3d428a4c87f11f0`  
		Last Modified: Mon, 03 Nov 2025 19:36:15 GMT  
		Size: 88.8 MB (88796418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6213908a2ce7c79893b53fc011ff630a7b872402b8c103fa1452f1695d90c41`  
		Last Modified: Mon, 03 Nov 2025 20:48:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0b72a5acf16f701073950b4b9a79dc3686a27ababbe60686566c370e0eb74aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340587b476d39501562fc90835d4aae8336953e6b261b850d337e248502ee23a`

```dockerfile
```

-	Layers:
	-	`sha256:8ba0ec5753bdeb715229bcb4ebe5861730cc84c8511580463b5869326a27ffd5`  
		Last Modified: Mon, 03 Nov 2025 21:24:43 GMT  
		Size: 192.3 KB (192288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15543194b052049140705869e646b26257d20f5896b3fce1af29a0c8ae46ff0`  
		Last Modified: Mon, 03 Nov 2025 21:24:44 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:46676c8b6008813b3a87cb4ff3b21244e37bcba3acb5dc5c2536be76731b807c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93595079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f65b96e94e3b6d51f2651e152c82935ddaaf017eb51c045313465660960fcbe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:17:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:02 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:17:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:17:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa10ab6a939fc7b57442bfd1592957fc4568b2b76c4a2680a686827d9c63676e`  
		Last Modified: Mon, 03 Nov 2025 18:17:47 GMT  
		Size: 292.1 KB (292097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801db4c6115aae59bd4317ca926bef2957dbc3991dbc119cde22a6ba6c9c43c7`  
		Last Modified: Mon, 03 Nov 2025 18:08:18 GMT  
		Size: 89.8 MB (89836390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba52f9939f556d69c32e01283b5aeb3dfc2c3230561386c3897f7f6c0ab7629`  
		Last Modified: Mon, 03 Nov 2025 18:17:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:de2ef73ca2a1c1de11462dd97270e635a369529d10b216d8f0779f08c9a0446d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fb95ae68e9e157c5b4853af6472029665a1eca6d8f7c86d3bcab0425eba85c`

```dockerfile
```

-	Layers:
	-	`sha256:b94ac7ca5b653bdb17e74343ea01b9cb0e461273900cfddc9dae4beb3cc6ab8d`  
		Last Modified: Mon, 03 Nov 2025 21:24:47 GMT  
		Size: 192.3 KB (192254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07c293383743f8be35492f2920000fceadcb180cd44283dd9cfa003a208a9ca5`  
		Last Modified: Mon, 03 Nov 2025 21:24:48 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
