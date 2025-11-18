## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:5ae59f994dd5d4202afd2c611065e66c373def57878df45c1d51f0a91c15827a
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:4fe9f0929fc18230658b1e361b00c5f81b79e687e33255f3d9bdc84efc1fcf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96058065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54565052355178919ee19b6d55c61ba3936ffe1816eb1e1f368e3055db095ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 02:39:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Nov 2025 02:41:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 02:41:41 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 02:41:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:41:41 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 02:41:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 02:41:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595dd90baf1f6b0875244206b370bd64838aef4070a6d01fe8afcb05cfb220c6`  
		Last Modified: Tue, 18 Nov 2025 02:42:08 GMT  
		Size: 291.2 KB (291156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed7b3373fee62cdb53f94efd45c65db5604e6edbc40b8d907723c04dd03d3e5`  
		Last Modified: Tue, 18 Nov 2025 02:42:20 GMT  
		Size: 92.0 MB (91964299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dad23f987ea2cc4314d6d4938356c846d69c6cf0b6c92b2a408b30c7a4da809`  
		Last Modified: Tue, 18 Nov 2025 02:42:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:654b50018ae5edb270fe93b675730febaaf16bc4ba48f972443295c853e6bc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a2b499bc755eafd4239c881b916ede45ab089a533d7d061ae1b76291ff6c98`

```dockerfile
```

-	Layers:
	-	`sha256:cfda7f4ec4f0b922116353fa5112b9c2db30a5f3fda1e6135116c2367a5b4a12`  
		Last Modified: Tue, 18 Nov 2025 03:27:39 GMT  
		Size: 195.6 KB (195612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7cec1792420f0775ff8e21670bd568c74d676ec8f1a4a934f528648140b9188`  
		Last Modified: Tue, 18 Nov 2025 03:27:40 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:349d4f6e23f5b81288516af6f9f2d969d6e59b771625f8d5d07572d3cc680ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92172187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb35ddb871a7349a8ae807b3d889cf0680df267f92b76e1d9aee67b9d2e281f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:15:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:17:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:17:37 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:17:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:17:37 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:17:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:17:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c4482514c487364c89881dbb9ebdc7d7bac57dfb17fbdb8495d80fe6a2986b`  
		Last Modified: Mon, 17 Nov 2025 23:18:02 GMT  
		Size: 292.3 KB (292321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c633503e301869c39a50f9afcfc1072f957a321783e002663d5e1707a7e7f16`  
		Last Modified: Mon, 17 Nov 2025 23:18:10 GMT  
		Size: 88.4 MB (88375628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222a655331c8651a1a336aafd3b2c028e1bb45689002f5e879025b48d38a2a86`  
		Last Modified: Mon, 17 Nov 2025 23:18:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:73e2c55c824d3ece52daeece5354024e87e15db5f7ab6dd33d811ae0428dcf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cde28aba22318f13805604e60e877786255521f8b8b47d18a270e1633445d2`

```dockerfile
```

-	Layers:
	-	`sha256:63f640f4cbb1ef51fe020b6d381ae9eede578af42ec162891dc400b0db22f859`  
		Last Modified: Tue, 18 Nov 2025 00:23:40 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:62f8e7a529a18bc3e1ed363672c0bf831b2cb8cb0424fcbb406f9a6c72462fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91625638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2185d6dff9827d7572e8fb63eca1c06ac2daa956149b96ec7a41bdd49810dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:21:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:24:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:24:14 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:24:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:24:14 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:24:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:24:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a808919869b5eac1c5aa51dcc1a4d1f794f6941b82617af9c03ef0f9b68aa98a`  
		Last Modified: Mon, 17 Nov 2025 23:24:37 GMT  
		Size: 291.2 KB (291209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a2c69f85dc047cff5b8e0c725d241fb21eed7123e04e156a844669a6e5e5d3`  
		Last Modified: Mon, 17 Nov 2025 23:23:14 GMT  
		Size: 88.1 MB (88112716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e2800f43857ea40aafbd04eb2b205ed0da2b84b5c2d49ffcdd9886fd9b2b90`  
		Last Modified: Mon, 17 Nov 2025 23:24:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6c79076e26790214bc1dfd66aefa32ed6f27a751268047a94995df5d9aee486c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cdc25e746ea922ee0785f70a9e8e108d1978fb9a2fa874f31e68fc5d89e985`

```dockerfile
```

-	Layers:
	-	`sha256:b2ca8765a4e14f63c43447a0422970e1899e616180e597c8ca42c631caeb9a8d`  
		Last Modified: Tue, 18 Nov 2025 00:23:44 GMT  
		Size: 195.6 KB (195632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3915ec0de937358cabd062b39274c21f423133798f2f730858b35abc5c19f994`  
		Last Modified: Tue, 18 Nov 2025 00:23:45 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:162ee19b96c9cc0758ae59adf6e63c112404ffa9a8df02949d8c25c4718b2eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91610086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae43fc49dd3293b6952a1e7d9d6f6363a7ee37f5c43cf475edccb3f431bb8994`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:28:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:29:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:29:42 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:29:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:29:42 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:29:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:29:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4705e9d8d4e575b128c7438d0226b1247b5154f6cf708ee238ec712fd22055`  
		Last Modified: Mon, 17 Nov 2025 23:30:08 GMT  
		Size: 294.1 KB (294121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72859aa41c7126c75b0eaa6f62530c6ab6d97e63fe3d290a8c1d237f80407685`  
		Last Modified: Mon, 17 Nov 2025 23:30:36 GMT  
		Size: 87.2 MB (87177738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bf71629ec91e8ce31312256996b7b695c9bdef7db83f55bab12b9fb1bbcbc7`  
		Last Modified: Mon, 17 Nov 2025 23:30:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:190c1300fa1e5125801bd49c9b8ac4ab996e5af4bf3ec51ab9a5b5d70ca52fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4388972220369226178672bdb964aaf77bfe9bb04e627740f585d1aee8da0865`

```dockerfile
```

-	Layers:
	-	`sha256:0bb05dfbb967105e4fd87a3c3c9e05002be7f8d5f7f0eed30671095577b3ddd4`  
		Last Modified: Tue, 18 Nov 2025 00:23:48 GMT  
		Size: 195.7 KB (195668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39a8b212cbc55cf8386c4f3fd34c0441d3f26406d0573ec8e0cc4538817a081e`  
		Last Modified: Tue, 18 Nov 2025 00:23:49 GMT  
		Size: 25.3 KB (25254 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:dc52086831508d153bd38ce4608b635aff99bfce0f7896038698fd2930faf0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93815623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4d2b4f6d6b617fefdfb4f99331c82d1b090bc0909c02195f5128edc5f2bc1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:20:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:21:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:21:50 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:21:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:21:50 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:21:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:21:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79de04292720e6ab7a32371b7751d02c5b767ec9b6672e3a2ef072cf691cca1d`  
		Last Modified: Mon, 17 Nov 2025 23:22:17 GMT  
		Size: 291.6 KB (291638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb363788838918ac7e550b93200cd675ca2501f3ca5b79cee14723fcfb2dfe5`  
		Last Modified: Mon, 17 Nov 2025 23:22:28 GMT  
		Size: 89.9 MB (89904896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d262e6dfda2b94c8c64d8867b702f4ad07864ee446e2ee097ffcfa7ef482093c`  
		Last Modified: Mon, 17 Nov 2025 23:22:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ccea0f18e08c6e529ebcbbc55adb33eeffece85bd185e3fd42e1d437eb83be74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47f8876b84b84a37d35e677402d638d2b2f7b298a6765e370df82a51784a430`

```dockerfile
```

-	Layers:
	-	`sha256:1d46f872f52efa4b494b62cd3df4b39cc67f8a394850296e0abeeeb78fd31679`  
		Last Modified: Tue, 18 Nov 2025 00:23:53 GMT  
		Size: 195.6 KB (195571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dce7605473bb7cdd0f9d754580de547fca6685979df2047c5a2adfcc46b693b`  
		Last Modified: Tue, 18 Nov 2025 00:23:54 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:8d26cc1869c309535976305840467e82c45bd6d4535114104700c84d1c02355b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523bd58cae1bd93286c3928e9439741d92301a4c8699e7e76016c2985f01f79b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:53:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:46:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:46:01 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:53:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:54:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2fe5b10161c1f9b62c4b3cd003499276af28b040fb63dd0d1fe07d10b87e7e`  
		Last Modified: Mon, 17 Nov 2025 23:55:16 GMT  
		Size: 294.6 KB (294589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17fd7fd0e8bf95c13c3a94bedc5db23eb0e60440acf59ef05963d43e52ee79`  
		Last Modified: Mon, 17 Nov 2025 23:48:37 GMT  
		Size: 88.6 MB (88638105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11c28816a0fdf9046daccaeec84916c84e12e3c1073273acee7d1838966f599`  
		Last Modified: Mon, 17 Nov 2025 23:55:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:b1be7eff5ce5b902239f3b7c48c66c3fbd7d0f05548b30dfadbc470d53e85b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188761088f8ea47295af53e3cc77f2c8c76838f485ff8120e4f0edd44bffa009`

```dockerfile
```

-	Layers:
	-	`sha256:f0a5cc617ab16b4681e043ab9e68e417b5e84ea98b02b8c3fcf193481d0dbdf4`  
		Last Modified: Tue, 18 Nov 2025 00:23:57 GMT  
		Size: 193.7 KB (193711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84321ee62f26f9a4d94c76402e1131582a267ca11435ab114f1214f8111fbb99`  
		Last Modified: Tue, 18 Nov 2025 00:23:58 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:dc6271a7e17999c6a2bc453d69f9c41ea4eff4b8c474850f901dca195f96fecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92927112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97802b4270a6812f09618872b2477561ae470c6f8decaeb4bc5584f739363527`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 01:07:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 00:22:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:22:22 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 01:07:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 01:07:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53fddaddb4a95a0fda848134afaa1e0fa3791bf6bfcd1e1997f4fb262f1a705`  
		Last Modified: Tue, 18 Nov 2025 01:09:23 GMT  
		Size: 291.5 KB (291513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec3a0230c2d0fb9a920af1a0e3505c5c46ba754e2ed64bb7c5b5268656905`  
		Last Modified: Tue, 18 Nov 2025 00:32:26 GMT  
		Size: 89.1 MB (89120201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320d80d06a8f50a9895bc552b1a5a9fb83f1bb18df5052d1212630277998f7b`  
		Last Modified: Tue, 18 Nov 2025 01:09:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:39d563a958efe1d65d88167023f87a8f336c231d6d19c28f359cc034d1bd0b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64195fcfa03a0513a64c795cae60b7d657d95d890635a552bee5978a4a7cfd3`

```dockerfile
```

-	Layers:
	-	`sha256:11f30fb7bce9e42109d13451a57e3e605d565454beb6de59ecd0dd104a89d946`  
		Last Modified: Tue, 18 Nov 2025 03:27:52 GMT  
		Size: 193.7 KB (193707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e040ae5be135b0fc900ff3c7b230721e5585936ed25761d06c9adaca266514`  
		Last Modified: Tue, 18 Nov 2025 03:27:53 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:d0d873b2d503cc79404437f1ae0e9ecd6d07e13bfd59ef4b169815bb555643cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94119468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42a1e37748151c1df0eb49f24c0aa17cca5b229bbe5b21aec31cbe2257f7d6c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 23:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 17 Nov 2025 23:26:35 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:26:35 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:26:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:26:35 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:26:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:26:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977560f9c1c40be75e83760a5dc4f823449615a01b2abeac3f8da400815487b`  
		Last Modified: Mon, 17 Nov 2025 23:27:03 GMT  
		Size: 292.2 KB (292157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4515f8b1d9cf2143fbca8f466beb9046119009ff0c9973ec41a536bfa5dddca`  
		Last Modified: Mon, 17 Nov 2025 23:27:17 GMT  
		Size: 90.2 MB (90177909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbedda227caf79d9e898a8f056b86f881a0d5a741e456e3ef93eb633396abfff`  
		Last Modified: Mon, 17 Nov 2025 23:27:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3acd61d3bab367ac1428bf05c7874dcd54552b778c3c1d131d1bdf33d09815b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a3ce662544a4656825d407c70c46b24d09caca9acaf9678d9bedfd0061662e`

```dockerfile
```

-	Layers:
	-	`sha256:0df2ebc83fa53984cee96775de60859558f52b90c945c63d63331ae17ade5aa1`  
		Last Modified: Tue, 18 Nov 2025 00:24:02 GMT  
		Size: 193.7 KB (193661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf962b5fd0d5a9f6cf13481c25569f076bbb1ab1a90318df48b6743d8c4b819`  
		Last Modified: Tue, 18 Nov 2025 00:24:03 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json
