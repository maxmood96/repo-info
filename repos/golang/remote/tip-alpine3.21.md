## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:7521aa889048a4279c7bf37efb82561e7d5709f3915732446b7ff062bb412448
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
$ docker pull golang@sha256:d7b37738f1bed09185fc555c146061867c13e03c1dd60ef64eed5f57044bf30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95610893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc028729ded32e4d9ade6967f5541b8c0d56af25324efb4894da149ae32abb32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 21:26:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 10 Nov 2025 21:28:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:28:19 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:28:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:28:19 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:28:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:28:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457e6c42a3943321184507a9a003b8c49338d9ce8ee030189b9a84e3623d87f4`  
		Last Modified: Mon, 10 Nov 2025 21:28:42 GMT  
		Size: 291.1 KB (291120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaf52c0c17111119e1092b7027d6d86d20ff4880cb34ac8f9ccc8cf394dc978`  
		Last Modified: Mon, 10 Nov 2025 21:26:54 GMT  
		Size: 91.7 MB (91677046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e685778335c434bd3bdb43883241eb9d20ce1b7c5f963a8901d62599a45bcaaf`  
		Last Modified: Mon, 10 Nov 2025 21:28:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:71353c7f40a37009e668e67f5c249eee2b91ed62e81d0c9b0952c17bf16facf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5753d377e700bd1d2007e1610c489c62c5035f2e9f0c62e9600b8a5670a9ce`

```dockerfile
```

-	Layers:
	-	`sha256:1cebbaeba1159c6cd3785ecb150c449ac79d3f577826325df5942f40126c8f98`  
		Last Modified: Tue, 11 Nov 2025 00:24:17 GMT  
		Size: 194.2 KB (194205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ec76eefada5971c60ae2acf8ea4261b25b11590906a5e31f61fea19768c1ec`  
		Last Modified: Tue, 11 Nov 2025 00:24:18 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:82e9a611be5df8e308ce084f916652360b70a7b889d7d1474279cf97aa819cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91753563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecee998d939663344888a05a8a385fdbfea755269eab4e7da66d930135e6e5ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 21:27:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 10 Nov 2025 21:30:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:30:07 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:30:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:30:07 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:30:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:30:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195fb5dbd463c0c9e1bc6f8a537b4dcfdc87d7c659caab0a0e544d0bb1f380a7`  
		Last Modified: Mon, 10 Nov 2025 21:30:29 GMT  
		Size: 292.3 KB (292267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26b7ead66116bfd52b5248a86acb096b3c8cd055af0b89507feb4bc7192ac9`  
		Last Modified: Mon, 10 Nov 2025 21:29:11 GMT  
		Size: 88.1 MB (88095670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57cebff1cf60bb0ee8ceb11dbe2dfba5cb9ddeb7d6a1c5b9ea26c6bb6e63333`  
		Last Modified: Mon, 10 Nov 2025 21:30:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:500ef4a54063c9ab565ab0d2a2ff8372d3c42adee952f096b958cdf9b9215984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379fa2e2d8373448196d3a8755a687ad3f74847fe8ae370c43d7e2e6ff45654`

```dockerfile
```

-	Layers:
	-	`sha256:4625807be13736cccd9e71d1ba1351055b455fa6cb21d374848142efdbe4d409`  
		Last Modified: Tue, 11 Nov 2025 00:24:21 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:c7ef3bb94e56a493c3eb0ed00582659cb908059ece31b5dce518ac9345a0f4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91232894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a84cada664a9e9d1c798366667053c44e70ba9be94de5de1487ad1848cfc315`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 21:25:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 10 Nov 2025 21:27:30 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:27:30 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:27:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:27:30 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:27:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:27:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be996cd079586a191e59137f87a626cbcd26ba447cfe2318979a6d51c81bb001`  
		Last Modified: Mon, 10 Nov 2025 21:27:53 GMT  
		Size: 291.2 KB (291152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80af05985c341b2243144191457637b935a05afcbc1ddf3359092401ff8e5eb3`  
		Last Modified: Mon, 10 Nov 2025 21:27:35 GMT  
		Size: 87.8 MB (87842973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734dd88ef7a88df38aa81589d6d47554f66d2bef080ea9ce1383adb142904122`  
		Last Modified: Mon, 10 Nov 2025 21:27:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a186cde87e8178453a62ad16720a5b6a3dc4f5353f47329b1abac96b69e2aa55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583422dd8667fc31d0a0d83f544f205fc7ae5ecdf07d4b2a54c4883db0d067e2`

```dockerfile
```

-	Layers:
	-	`sha256:a95596c4fc39b45a86993c8d28b16bcd758e2580d9a20d17a8775e3deb075560`  
		Last Modified: Tue, 11 Nov 2025 00:24:24 GMT  
		Size: 194.2 KB (194209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56c28fa9949285245dedb4be473c69f72a8c7e3f456f9d5230fa7cd9d0efad5`  
		Last Modified: Tue, 11 Nov 2025 00:24:25 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5ac87084b490a1cea16323f176af4e274a751bf913f03458bbd2f87e40669ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91205014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf1a51b011cb5cb6e781df95d42553ce53ed456943b61da1854d0ca94551ef3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 21:26:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 10 Nov 2025 21:26:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:26:14 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:26:14 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:28:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:28:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27df81d9bda05483d19cd5b85ca60c2ba9def6f035c306200350b33a529a753`  
		Last Modified: Mon, 10 Nov 2025 21:28:41 GMT  
		Size: 294.1 KB (294056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc394c4671e4765368842b5021bb1bdf0fc1fb8ea3eb886019790f8b58e10a`  
		Last Modified: Mon, 10 Nov 2025 21:27:06 GMT  
		Size: 86.9 MB (86918448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b005d9b2f3822ff148237d2db9afa10a5c61f011def5892abb0ff3ff7c977fb5`  
		Last Modified: Mon, 10 Nov 2025 21:28:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8d35084b1c51644b3ef6cc6d9f88799952aa672804a1eaa1006252d7ed291323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ea67c2b8af225931b08f6c189413f1c29c5234d4f2e97431ae44a9801226c`

```dockerfile
```

-	Layers:
	-	`sha256:19070c000b334da9c43bb7cc9e989fe3655db61fde5a170d43a260e746df472e`  
		Last Modified: Tue, 11 Nov 2025 00:24:31 GMT  
		Size: 194.2 KB (194237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0641fcdfcd5972db4adf1edd7a077af68c2f9df4a62dceb2394a97b32a061c53`  
		Last Modified: Tue, 11 Nov 2025 00:24:31 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:e24be7365af67004ed9c9a16eb0d6ec4746d645dcc503ab1ecf3ec4a22211fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93417865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623ae18ea9655a3abfe5c1870d1e6082f39401bc4decedc361a131b146515d7a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 21:27:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 10 Nov 2025 21:26:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:26:52 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:26:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:26:52 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:29:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:29:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073c2967c5ba246ecbb5d1dac4d00f834605b5766994058354af062955766c2`  
		Last Modified: Mon, 10 Nov 2025 21:29:39 GMT  
		Size: 291.6 KB (291593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6760ff784f4cb90e20d85ded90c45e254a2af1adc9c4a815538370e9b9f35c`  
		Last Modified: Mon, 10 Nov 2025 21:27:48 GMT  
		Size: 89.7 MB (89661412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a0913dfaa1590bf4be3313d19ca42f75ae45a7a8022712ca31dbce472abc9e`  
		Last Modified: Mon, 10 Nov 2025 21:29:38 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:ea43ce4911163f75e3df3fb569fee05c5716948b809211d6e0b1ff8846df2423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8e922b0b188d59fdba0dc821fad934fef29b38c6d090f34389b20b3653214`

```dockerfile
```

-	Layers:
	-	`sha256:040f9e2b21cb0d426d18c9ad189cdbbea97bea639b89125bf3e7a78c3fa11864`  
		Last Modified: Tue, 11 Nov 2025 00:24:35 GMT  
		Size: 194.2 KB (194174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323b50d878afa82e56ae3686a8726049f3a5fa98a83ef18c2690d1f1f1bdd2b2`  
		Last Modified: Tue, 11 Nov 2025 00:24:35 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:cc755a2c89f18c0e0e5dcf5cc0912cd235a7c1df6ac42ed3487dc5d3e18d295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92241899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f2f056f8a671522716846b0746ca3007d68b5e2057757963a13afc72ba5cb0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 22:42:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 10 Nov 2025 22:33:11 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 22:33:11 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 22:33:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 22:33:11 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 22:45:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 22:45:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d4fe1309abf01cc3b396605f91d335f53a4bab7cc75d36d37b45e30befc347`  
		Last Modified: Mon, 10 Nov 2025 22:46:11 GMT  
		Size: 294.5 KB (294540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f48426cabbc07e67f83c1cda5c24171abce6e81b7fca3ad79e01d21f527b41`  
		Last Modified: Mon, 10 Nov 2025 22:34:40 GMT  
		Size: 88.4 MB (88373126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd2f437ae8f5a7ed4271676017b36bee34b31583e893575b2b75802bec61d12`  
		Last Modified: Mon, 10 Nov 2025 22:46:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b67f1eb40e5ac923a261a7c89c37003e9e07c549d5c4afe879457373350759cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c65df035e20bca86c9f52f2da27366e1d1b2de514fb4effc31e3523969c5ef`

```dockerfile
```

-	Layers:
	-	`sha256:f74ca84ca6f11d42c7222bcf5359f9ad88ef4173a8c5377d6ca63a0b8a3b8c5b`  
		Last Modified: Tue, 11 Nov 2025 00:24:39 GMT  
		Size: 192.3 KB (192292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc25c670e8c7f641bda3f4f63eac79a9564c7ebe452b1db8b4e8c2059d95721`  
		Last Modified: Tue, 11 Nov 2025 00:24:40 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:76c65da501e7fc9f81e40040f7c5c3aac6cae33276b365208c3dc4da05038ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92519599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea48ed3167166249f9c469919c7847c32ad56a1b6efbc4611042d22d8823ef06`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 10 Oct 2025 20:46:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Nov 2025 13:18:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Nov 2025 13:18:22 GMT
ENV GOPATH=/go
# Tue, 11 Nov 2025 13:18:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 13:18:22 GMT
COPY /target/ / # buildkit
# Tue, 11 Nov 2025 14:35:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Nov 2025 14:35:07 GMT
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
	-	`sha256:29ab1621244769c0984c93db0d3fc511cde215b22a38f39de50fc1b81bc4fc2d`  
		Last Modified: Tue, 11 Nov 2025 13:25:39 GMT  
		Size: 88.9 MB (88876978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1432bf31ed5b5d4cffe66838210f2d6483b8763df2a35e867e443a5daf6f1e`  
		Last Modified: Tue, 11 Nov 2025 14:36:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:868c6b147d0d3934396b86b5655f9e0994c2b7413d131f0ff34dddb90d3925e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585fead5f14a9505ed7b42a73397aa99317a3345e6ef94fe61a6339badc0cfce`

```dockerfile
```

-	Layers:
	-	`sha256:fa7dae19ab8383acaac50445a80dc1af72139a6aaca26fa12094581b076bc8db`  
		Last Modified: Tue, 11 Nov 2025 15:23:44 GMT  
		Size: 192.3 KB (192288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9bdd4e84a86d804378c097be5f5db812c0f4f444d0ab5c0a96988b39652940`  
		Last Modified: Tue, 11 Nov 2025 15:23:45 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:b2fec28b00df6b8292f5389b68a8382f744e1f6bd60e0e48875466e0dce493c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93647989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0006625fa086fbbb2fa8099cec8e73bac24b941897ff845c19ea7200ddd0e956`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 23:16:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 10 Nov 2025 23:05:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 23:05:52 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 23:05:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 23:05:52 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 23:19:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 23:19:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cac43b2abcc0a681fc9d82cca717fdd907d55e05a8120f614bd24570d02301a`  
		Last Modified: Mon, 10 Nov 2025 23:19:19 GMT  
		Size: 292.1 KB (292107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64f47020d1f3aeb3d5d5264472a9b269aff1c59728387c987b54097fe8c0fe`  
		Last Modified: Mon, 10 Nov 2025 23:07:54 GMT  
		Size: 89.9 MB (89889290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f43a4fefb401dacd50dd882e9eaa23aff57b0c499cb90ae7393c61274e0238`  
		Last Modified: Mon, 10 Nov 2025 23:19:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:29914360edb9f9bda84f839e41576a453cc2a892271267e49f521ab06b3ebcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e8da415d4c6087a9126bc629de7bb00ec28233d63027619271713277aaf9a8`

```dockerfile
```

-	Layers:
	-	`sha256:8625ad0a7710dbd138c804218761fd66e3b42544913a57f63056ac78ce0a51cc`  
		Last Modified: Tue, 11 Nov 2025 00:24:43 GMT  
		Size: 192.3 KB (192254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbeaa8d334f14d85d235800ef89d26c5eb75396dd017501de8e04235b6032d6c`  
		Last Modified: Tue, 11 Nov 2025 00:24:44 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
