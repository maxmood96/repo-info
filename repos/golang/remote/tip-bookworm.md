## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:2266434b37bf3cf755ed62b0f85575c9a7e53a4d952007661e90d94c6d177e48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:889210c96ec90580cd904de0343224a8d647370e5a8778549001a0e5cba06a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326705545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92fe7df4aa79609000865f841c4ca6b09e6acb4c605dfef1f461251feca3fbf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:59 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:59 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:59 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:42:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:42:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213a022e7dbf0944407c7890c4a766cbdbeefff784bb87deccd5c4a090febe2`  
		Last Modified: Mon, 20 Apr 2026 17:42:29 GMT  
		Size: 92.4 MB (92448881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9800fe1d00fbf93fa3af2c224e36eef8eb15b87c8b6fcb13141f73eb2f1ed`  
		Last Modified: Mon, 20 Apr 2026 17:41:31 GMT  
		Size: 97.3 MB (97333404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ffb3a89b311afb7ac3b6b7ce535bbab48a667c516cf04bfbad86cb8d9eca02`  
		Last Modified: Mon, 20 Apr 2026 17:42:27 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:844974788ed4e4a0f5d2c5d64d367d592157af787e660668a36cde3cd641d1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203502be8c45132a3e6d73c76aa4532c1c989d314a45033d429d17e7887074f3`

```dockerfile
```

-	Layers:
	-	`sha256:33351cb41e8659171968e07218dc327a037cc92e9088ebd6bd36d8d253f4a54f`  
		Last Modified: Mon, 20 Apr 2026 17:42:27 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70fab7abad6ed23d51ec58550d4c03daef4633f2a7876b962d2156f63f05dd2e`  
		Last Modified: Mon, 20 Apr 2026 17:42:27 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:c8f3419bccec4f99fb4b861927020289214684f4d403b6fdaa404a5586800a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285274565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586919609d66f7d4d202a8eb86436d76421dfcdb48b42648c01158a6078d8cfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:21:08 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 05:21:08 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 05:21:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:21:08 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 05:21:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 05:21:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3960cd47ab70e092f1d1162d4a33a761e2cfa64e09c3ca3118416ced1e6f99de`  
		Last Modified: Wed, 22 Apr 2026 03:52:25 GMT  
		Size: 59.7 MB (59652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02024d7a65cf0d89b82c9345aa490094390ad4f0557726b9b7b3894307b9880`  
		Last Modified: Wed, 22 Apr 2026 05:21:35 GMT  
		Size: 66.3 MB (66305373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42fcfd73df1c3c4e864c147debb0154bf1e1c38912174f3d52a47a654a9641`  
		Last Modified: Mon, 20 Apr 2026 17:43:22 GMT  
		Size: 93.2 MB (93162179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb94b97e6e92863520d53baf2e775a278822ac76ddffe3e5de716799cc6243a`  
		Last Modified: Wed, 22 Apr 2026 05:21:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bbc417ce1151af1c8d38b1b1713f1ad439ba2ec2996aaea7adb9aa078b950f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99165211a8777c630222fda280a624a290612482aae7fca153712fef4b581907`

```dockerfile
```

-	Layers:
	-	`sha256:8c1a6a4325ac1c97de4456e353bf1b58ab707a36d30e729150f18edb59eac758`  
		Last Modified: Wed, 22 Apr 2026 05:21:33 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b766353f539c4d07862459355c3710fd7e56b39e7450e0953a433e408930187`  
		Last Modified: Wed, 22 Apr 2026 05:21:33 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:db7a3b3efcf4d077a41c5198aa1ea66b8b013e62c72aca858eb24ad04a97cb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (315004205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c504c9d4581478f19b52cb84d9a0ffc4c9a011c59dc4a428029af2e20dec00`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:18:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:19:59 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 04:19:59 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 04:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:19:59 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 04:20:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 04:20:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fb534e886bf427ac371d8c2d457637ed5a24fef53b45d473e69597dc521290`  
		Last Modified: Wed, 22 Apr 2026 04:20:26 GMT  
		Size: 86.5 MB (86521317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9da8d3894800a39f60fbfd67e48a2654efcedecf176b3e40f1e07ab0291557`  
		Last Modified: Mon, 20 Apr 2026 17:41:33 GMT  
		Size: 92.0 MB (92020630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97ed993f2c6eedd38c78ec30463409995f762b07a9ba4bf32f4f22af067097`  
		Last Modified: Wed, 22 Apr 2026 04:20:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5ce630a7107476e0800847098cde83b3024cead44248040a996ddb53820d4c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4939b64d00c1108fc9e2359b7dbee3347606fb9f814e02158a1db3c8b94c508`

```dockerfile
```

-	Layers:
	-	`sha256:fb59289dd7152fb74027a11c004b53dedd5ff74869871dae6f32edbed23c48b5`  
		Last Modified: Wed, 22 Apr 2026 04:20:25 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197a5797c7aa500d820d26ce1c11d5c930648436228c8495484fc225342cce28`  
		Last Modified: Wed, 22 Apr 2026 04:20:24 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:a9481c679392ab1c138f17afd9d1addbf11feb1e86d1a357bb0e749c88ddf11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325528597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd3a8dc5476adfa220c75b79b5e0fc54476b54e917a5b2c80854f546e91182a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:40:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:43:05 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:43:05 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:43:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:43:05 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:43:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:43:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240fa1f3927770a46d24419f7704239ba70e841afdde2d9e2629af344b11c262`  
		Last Modified: Tue, 07 Apr 2026 01:45:49 GMT  
		Size: 24.9 MB (24871973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fefd2d4d18c0e4a1f706c31af7edb1bb87765de90f366b612fc4f713dbbfa`  
		Last Modified: Tue, 07 Apr 2026 02:40:53 GMT  
		Size: 66.2 MB (66234451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8453228998a1b67dc27de1157cc3413c8d1c8d34f0696502d277cfe983fc6f85`  
		Last Modified: Mon, 20 Apr 2026 17:43:34 GMT  
		Size: 89.9 MB (89871589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0ee3233bce23292707dea9900b4db989f25efd70edf364d9cfceefc1e3441c`  
		Last Modified: Mon, 20 Apr 2026 17:42:46 GMT  
		Size: 95.1 MB (95072511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a5f26f35fe3874aab5513ddfda4ed97ec81faf6ee0f7fd3eda03d6a494c02`  
		Last Modified: Mon, 20 Apr 2026 17:43:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5c0d0a2acaf68b371cf5e469b9226c8949733cc1aaa744d4a2bc70f0dbb48de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6989307588fdd517b1a7d2c066f50ae6b6c7ab59d2a586dc6066cec59f86361`

```dockerfile
```

-	Layers:
	-	`sha256:68fc9ea05fae7a45cf87ce30181947eead734944c40e9a755dc18abe3cb428bb`  
		Last Modified: Mon, 20 Apr 2026 17:43:32 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248fe5f963b3fd9e7a20f9ada192f10772f59f55c28fb18c95e216b37d0c8f09`  
		Last Modified: Mon, 20 Apr 2026 17:43:31 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:4b2f111fc919134cc980212a8705b54e7aeebc78d2a44d7b603920d377af601f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296684259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81e50138bd8424a2f04948de90eb399aab3c3ae3f62326ed1af930270899188`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 20:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:52:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 18:01:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 18:01:39 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 18:01:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 18:01:39 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 18:01:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 18:01:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5370b42611bdad35bb24b3e5a6a342f00eb8523dc8562b7babeca6f19608f4c`  
		Last Modified: Tue, 07 Apr 2026 15:01:37 GMT  
		Size: 23.6 MB (23615262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df968e8deea10f7e740272ffa34126abe9d9673e41bbeb7f3f0d785055e19a4d`  
		Last Modified: Tue, 07 Apr 2026 20:28:18 GMT  
		Size: 63.3 MB (63310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cf83c0e933a4e8a498aae736ebf10a823fd9ecc755d47233e566e941c9893a`  
		Last Modified: Tue, 07 Apr 2026 21:54:45 GMT  
		Size: 70.1 MB (70051233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d97d132c4cd2477f08383bdb25847164f9927a3e74753805edac12b4cb96c73`  
		Last Modified: Mon, 20 Apr 2026 18:03:53 GMT  
		Size: 90.9 MB (90924954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960bc4521c730013fe19bf0192469d48d0f76651d21fefe84993706488c12b1b`  
		Last Modified: Mon, 20 Apr 2026 18:03:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e3f711c00deb2ee5af06bb0bffceeca595836423e20ee1c4748a1e48db5ff3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa0790ece22e1755db8dd1df63bf9c45c6210e7a1f70b1663eb08bd0c1e9ba8`

```dockerfile
```

-	Layers:
	-	`sha256:898a9c17b9ebe7d66a4d6cc8ff2fba036980ecc54c060e861cb70d9b8f63ae87`  
		Last Modified: Mon, 20 Apr 2026 18:03:44 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f6b2bbd8e56a34283df84cdc3625ea6e69a2128d5cde4f19f01931c05275bdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332189765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c2dbc1c9667a411c6501c9e684c3f24c0be04f3311d646c3c5dc752337143`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 18:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:28 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:28 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:41:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:41:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a522a501745b6503b15f6badc6170d6fa2321f26576c47b363acd8cb21b2ee`  
		Last Modified: Tue, 07 Apr 2026 04:21:54 GMT  
		Size: 25.7 MB (25671577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f98ce990098f8650217504a159d9031cc264dd29e8af85f749d78eacc319c5a`  
		Last Modified: Tue, 07 Apr 2026 09:51:25 GMT  
		Size: 69.8 MB (69846122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f67f0a7bc2638109117ec62f84bf4d06b91348ec6d8486011aaadaa5f42f65`  
		Last Modified: Tue, 07 Apr 2026 18:22:57 GMT  
		Size: 90.5 MB (90462415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f72075717c40f723c05a62a7b4daebee738f45ad2854cdb0f9f31a6113d444`  
		Last Modified: Mon, 20 Apr 2026 17:42:34 GMT  
		Size: 93.9 MB (93872555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88efcabef6e283d5bcc78bb9abfc58b745bff2a831e6eb81d3934de39ad4fc63`  
		Last Modified: Mon, 20 Apr 2026 17:42:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b257830361dbaaa4e20a51df708340943edd76348f581547aa9fba6c03ffaf6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a02418715350b53dd1093608245c97af0473616d3f0ab9d95d1197ebf5d6e3`

```dockerfile
```

-	Layers:
	-	`sha256:b7ab6ec7c895b0149d80daab238264aa3a54dc147123389430828974ffd12446`  
		Last Modified: Mon, 20 Apr 2026 17:42:32 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9649b64ee7d21b941e87bac7c925a4b4b19f24fb3f9ab0d0100a99cdbc21a1c5`  
		Last Modified: Mon, 20 Apr 2026 17:42:32 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:0f32ffa23b1e4d64e216da89d8eab80121611fbd66327bd4c9432e0941db4aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299590934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef167b37feca9b4d3511e66d0f66dc674c2bdd612311f171f67415c4239d3839`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 06:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:48:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:48:01 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:48:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:48:01 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:48:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:48:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47976b1872c5d8fc1ceda4d073087f195be5506b083608f5c0a6767f6b55978a`  
		Last Modified: Tue, 07 Apr 2026 03:04:32 GMT  
		Size: 24.0 MB (24033635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3377e46a7f95ad649f4e145572c4253ed3ebf1b9fa463b58c96cf8b20d651ac`  
		Last Modified: Tue, 07 Apr 2026 04:55:04 GMT  
		Size: 63.5 MB (63501358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7550815663570f840c3f2383dbf4c81d9f32d7c2cabee708665295a431772ce6`  
		Last Modified: Tue, 07 Apr 2026 06:02:24 GMT  
		Size: 69.1 MB (69055249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc40b99896e610d7e8bfd78ceac0447cbdeee9aed83f1c52c72fd167c0ef6be`  
		Last Modified: Mon, 20 Apr 2026 17:47:23 GMT  
		Size: 95.9 MB (95852451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575b3e4ed163414ca975e97fb9fd437d3b7cb3c6976c21199cb2a188b1896f65`  
		Last Modified: Mon, 20 Apr 2026 17:54:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ce55747bd03e724f27e94af803b92784f2a0200e9a3282dff0a099dd65ce32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c80668993ee8890fe7a6e1a7ff6a54c63a8d995612e241ac34180470f89cd3a`

```dockerfile
```

-	Layers:
	-	`sha256:18742df30a66a36a0b0a20a5701b6576043d772527da6fc65e73f1ca37907f64`  
		Last Modified: Mon, 20 Apr 2026 17:54:36 GMT  
		Size: 10.3 MB (10329539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07fbf68e7bf7fed1534a06a22cdefa81b6b1c567e0f7013ce2444ca7de732bf9`  
		Last Modified: Mon, 20 Apr 2026 17:54:35 GMT  
		Size: 28.2 KB (28212 bytes)  
		MIME: application/vnd.in-toto+json
