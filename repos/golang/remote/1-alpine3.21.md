## `golang:1-alpine3.21`

```console
$ docker pull golang@sha256:4f3d3b4f50212b3753fa50fb388edcc3226547346c4567b31deabdb75ef17698
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

### `golang:1-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:72ca7a88d35efa6e9956365a85e1e41620b9b0356df73e13809ed986d56cdca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63965993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7748fe1737c417bfcddc2099dd59106d539c7f835bbce48d95a2ac4f7c83a42`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee3b9deb6c3dac01dc4faccc31d93842683bf5558d87b827830fc0973c7538`  
		Last Modified: Wed, 13 Aug 2025 18:04:52 GMT  
		Size: 282.4 KB (282418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f14ba6ab6da27b694d29366005d5acd947c8fa8e9f1ebbe0ad9093f87e274c`  
		Last Modified: Wed, 13 Aug 2025 18:04:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:01129109c6e361f80047956031e7beac0b0cc124d80ebc387885bc80838b587f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 KB (215802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea3ffdb6552b9e4630f7f4e632905d350b3f1917b9ba2038d8a6f2b480b6200`

```dockerfile
```

-	Layers:
	-	`sha256:5069763c5c3e295dbc286b0f4ed762e55fa975b46305c8380a5697de06f4e389`  
		Last Modified: Wed, 13 Aug 2025 20:22:57 GMT  
		Size: 191.0 KB (190952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afd836365cd74e7acc9ab3904bac3a445deafeaace07be117a2d50d2bccecbe8`  
		Last Modified: Wed, 13 Aug 2025 20:22:58 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:7d16881d5d6ad6898d99689132592a75978ee9875fa82026f30c9f8e15f6d96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62624083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339864a4774d532227366c267511209c32865c56f3eba95678632c7fded4d5ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4a214d6543aa5b234ca6b16aa4d8e27cbc22cad32bed5ef48890ed7409c406`  
		Last Modified: Tue, 15 Jul 2025 22:48:38 GMT  
		Size: 283.3 KB (283275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf9467532185eee7488f7e36e8f4821d9ba905b6d1629af2856b92a090931c5`  
		Last Modified: Wed, 13 Aug 2025 18:04:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8644001c11f84d441b1b745dc01781edf8e801b643cbc4c67531183c1dd2a322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a60d048c119b0404da5873d69b48a6d4e7dd16b028d3c1335d375c324e0a77`

```dockerfile
```

-	Layers:
	-	`sha256:1e5bb5f191b2af853d7035a81eeb95f727a5466816cea293a401e4f7c9a6ef5b`  
		Last Modified: Wed, 13 Aug 2025 20:23:02 GMT  
		Size: 24.7 KB (24736 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:b8463e885461ec8c083d4c61be157a30858e2d0345fe8adb4e1348018a12c06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc06cdb6f3a31a82f0c1e41605bdd6b9cfe1482c24cbf6551cc899a675601af`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce1ad2f4fb08bb90f837004e5025b472d374435573f34a4ee7d7287172cfa5e`  
		Last Modified: Tue, 15 Jul 2025 22:36:22 GMT  
		Size: 282.5 KB (282462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166c0e3c20ad2ec3d2ae38755669929989f426a5d40574694a99b29ac0401f62`  
		Last Modified: Thu, 14 Aug 2025 04:31:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:018b14a089ebfdad5d2cd6a60b3de4a7c2667d047188b3ed0fd817583b4ceaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 KB (215926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263835865258dcfed358472a8883f435ad2b64af752c5feb4dd715d82116544f`

```dockerfile
```

-	Layers:
	-	`sha256:62c8bd7c1646d761de42474a7174b57ddb2b9c03fa76f93666cfb58d19995933`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 191.0 KB (190974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e3ced5d0c07f05f0f6d9082de2c7d04f5ecb22225d21225162798ca6473a49`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 25.0 KB (24952 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:848b554ffc07082bc78b5b3e59331144b50fbcf45246bfaaab0372c56bab65a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61827356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff46b2993640e8bdd65e09bbe4c3222ec369ac4ba4d28efd41869853883b45d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80bb7562bd7e03fda0615c89df2976c21bcf7fd34bd1bfa24010374df289e7`  
		Last Modified: Mon, 28 Jul 2025 20:57:12 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42305f35c321c9ebe4b4d42465bf127bead4a9811ddcbaba7c9dbcc8172565bf`  
		Last Modified: Wed, 13 Aug 2025 20:55:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:6551ae35dacdda99599b594be0de9147b7fba5d6858a0acfeebbbb5b9f518db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 KB (215992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518f68a243dc7177e9b894f0da0ce7604355b29ff425eee4b1c3ac0c6bd9e515`

```dockerfile
```

-	Layers:
	-	`sha256:9eefaf9b47f2b0149b33d12bfe2f23cffeeb3a1ca51f5cf9726faeb9355af8e4`  
		Last Modified: Wed, 13 Aug 2025 23:22:51 GMT  
		Size: 191.0 KB (191008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0433932866c258028cf7ac8a9f0c21fd9dcdfcd47912d8bba7d3926f2e643c8c`  
		Last Modified: Wed, 13 Aug 2025 23:22:51 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:b6ae55918d847924a00d6734c873fa9631fdbcbb9ec9d6edafc5ed80d353c35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62506873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d1c8339be74959e14ef53065b12d2c77e5727eab258eb416afa17411834fa9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b5a8da574818c2206432d630c8f4dbe622e8f74e1b2af340e007bb258b1eef`  
		Last Modified: Wed, 13 Aug 2025 18:04:43 GMT  
		Size: 282.9 KB (282892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c63a4b9dc1f72141c9a2ae757dabf818be084da59430ae2f1f1200a26ac66c`  
		Last Modified: Wed, 13 Aug 2025 18:08:47 GMT  
		Size: 58.8 MB (58763097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cc8e80cf5d02374b2d1454b40a5a4a36aadabd2963406444511bd57352cdaf`  
		Last Modified: Wed, 13 Aug 2025 18:04:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e1c357d03afe49355fb136af08229633f35c70fe3df4893ff13ee070126660b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 KB (215727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1401a5c3029f5a01227610479e5dd2fa70f81fe55a4f1712e1af9e0d0053c1f7`

```dockerfile
```

-	Layers:
	-	`sha256:f4e6bcbd5d5a0af044d6ff2c3794ca1e29d3e72cd782ad0b8ee6aa77eebcd54c`  
		Last Modified: Wed, 13 Aug 2025 20:23:11 GMT  
		Size: 190.9 KB (190913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58d439250e63bc3e307ee60695776b16c7cd41413ceff0ea385b506201950f0`  
		Last Modified: Wed, 13 Aug 2025 20:23:12 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:02c518784b08424716ba5a9791f5f1e755b570bd806c42130057975645dca973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61889444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201742414c6c47736ad4add3fec8682cb6afeb940eb3da5a3a93380cb82725bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4292e2d4d9d8706c1de48009e1d142646f4d2a8bd05fff7fc3f70c75ef02d1c0`  
		Last Modified: Tue, 15 Jul 2025 22:37:55 GMT  
		Size: 285.1 KB (285061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1a509af7e1983d5af0a27067a74d97bc4a16e0f12c5a932a58a49bd2b24ccc`  
		Last Modified: Wed, 13 Aug 2025 22:25:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:968643a5193876792c13f5f742250fa722c0ca96ec285284b752437a346adee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 KB (213947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be4a9870b9b6ffc22ac0619f5a4c2fc71ecb5c3b944f195a5bcf45f50db497`

```dockerfile
```

-	Layers:
	-	`sha256:6435ed431726eb7b976d72a31fcc27ae09423f5fc48b83528167e689700c7461`  
		Last Modified: Wed, 13 Aug 2025 23:22:57 GMT  
		Size: 189.0 KB (189049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:539d924c69b9f9e2b06718be49033c5716400d644a8c19e3e361e61c02695437`  
		Last Modified: Wed, 13 Aug 2025 23:22:58 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:f4fbf38e912d45ca436bd349df171ee6061deba8e28d0dd661dd82897bfd8c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79961536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0832208b022cea6287b0a7da6eb3673500ace76146bc31bd5b9617574aec0f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 06 Aug 2025 19:37:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Aug 2025 19:37:08 GMT
ENV GOLANG_VERSION=1.24.6
# Wed, 06 Aug 2025 19:37:08 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Aug 2025 19:37:08 GMT
ENV GOPATH=/go
# Wed, 06 Aug 2025 19:37:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 19:37:08 GMT
COPY /target/ / # buildkit
# Wed, 06 Aug 2025 19:37:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Aug 2025 19:37:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3100604e2ac3ab2afb5cfbb5b614bf8a221677bd8062fec6e7c8d427bd3a227`  
		Last Modified: Wed, 06 Aug 2025 20:38:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e5e5f6644186218e1667c5eff841df971a4b7d38b5694f81df95f4f78b88d504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 KB (230241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647087753658ce1b678a8e20d72a8f986921116248de25c9bd688b8eb0688b8c`

```dockerfile
```

-	Layers:
	-	`sha256:20cb2e25ec5fd07c59d04d285f3bd3a6642f39f9ff61ca5588a4a5784464ac5e`  
		Last Modified: Wed, 06 Aug 2025 21:49:09 GMT  
		Size: 205.3 KB (205343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c76f9dc7f0a0b48a2923b0beb9339c42c8fd77345b63eedcf03720c1b7f6618`  
		Last Modified: Wed, 06 Aug 2025 21:49:10 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:402afa3b1b03989f15e6803811fa8c40de3f5359ae3d28f4de7e50db6cf54f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63121484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770943616252b605a87c1a97fbfaea82ef2c8dfc4469a03b4d3d626eb1b6a1eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7c2184ed1d560f97be7198cd6f9baa12de8a0aff6bbb89596217c942ed2797`  
		Last Modified: Tue, 15 Jul 2025 22:45:47 GMT  
		Size: 283.4 KB (283425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d71585d875825b8d91de69623227272b092380893047410ee87078dcf4cf614`  
		Last Modified: Wed, 13 Aug 2025 22:31:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:73877d1beb2b07801a0ab2a8ccd6e74153caa378666a95facd763429a61ed840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 KB (213851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8363c55d4cffaa2f8056efc46613dadeff7df7d7c69de699361af2adc4da370`

```dockerfile
```

-	Layers:
	-	`sha256:1ecbcf5af5696c51b7c851eb3ee203b1b0c0145487bc41e8c2c12dfc652d3d2c`  
		Last Modified: Wed, 13 Aug 2025 23:23:03 GMT  
		Size: 189.0 KB (189001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e9b932d9b52ad8282dc09afa4fb60b9565ccce041488165a4407bbf01d4be2`  
		Last Modified: Wed, 13 Aug 2025 23:23:05 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json
