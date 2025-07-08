## `golang:tip`

```console
$ docker pull golang@sha256:de7a6fdda2b82799666420fe0233479e5efbde0905bcce0e0fb7efadaed2c204
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:5fc0bd6d1572db5af3f4dbf5d208a1d1c741f0981904fc36be20852cef186866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312355947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d3d759d4ca751b6853ab44d953175efa215b9692be343c8d7a86db668ff3a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5b82d8a573c3acce7a04551db2d944176e3a323c1e732b84d94f5cac7f8dc7`  
		Last Modified: Mon, 07 Jul 2025 21:08:08 GMT  
		Size: 92.4 MB (92354808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9b1bf1df4ddb6cd2f3ba43fc263309f8c370fe86f15d3de62305a26c4885e3`  
		Last Modified: Mon, 07 Jul 2025 21:08:01 GMT  
		Size: 83.1 MB (83086126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cada90faba1dc027228e435444e686275e362a90928927c155229077242cfd`  
		Last Modified: Mon, 07 Jul 2025 21:08:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0fe2cef4175851cfb80ec7de4a474d7e8992252320aa531f992c5e3697ab2885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20d8dfa64d7949bad077ada91878ad9d103dfb472ce852692fc552428229210`

```dockerfile
```

-	Layers:
	-	`sha256:811bbc09a47872aef21c438727f436960cf80dcf95cbcc0a5e1983fdb80f5cb1`  
		Last Modified: Mon, 07 Jul 2025 23:23:47 GMT  
		Size: 10.5 MB (10488745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb809233ce0d419338013771e949f410d4c39b1b527c6113ec6441ef98960d2b`  
		Last Modified: Mon, 07 Jul 2025 23:23:48 GMT  
		Size: 27.7 KB (27658 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:e9108b063a022cd708dfd72c4635de4e3ee463bb9e0ebb4a3295a3f317171a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272182687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e99b164a1dff39f502707a59b6f7f61bb4c3c6d421418b89d3cda176754b7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01db66a5672ae3586307aae98741965819f3d140302c02b7d781087e66393285`  
		Last Modified: Tue, 01 Jul 2025 21:45:51 GMT  
		Size: 66.2 MB (66208443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69fdb869efc0a02a2300329eae27592000268e157c8997d8c67d1e2518080e9`  
		Last Modified: Mon, 07 Jul 2025 22:02:14 GMT  
		Size: 80.2 MB (80181079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aaad51db2df7b07ff5fa6b4966ca73704e7a5fb726b5d5bac12085fedd7603`  
		Last Modified: Mon, 07 Jul 2025 22:02:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:e3a1ea0573cf2c8e1bd125f8c4cea522c266ccb42a179872c27d6e87dc34bd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10323241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397f31ce9b6ef1e01bbb9993e84f36ed4aa5111f8b9550e8ccb5e4765a16d865`

```dockerfile
```

-	Layers:
	-	`sha256:a535dd446ea8a40aab7d946fb1bf2e03c0b41230efaa106f96f66ceb8e8f5fa2`  
		Last Modified: Mon, 07 Jul 2025 23:23:55 GMT  
		Size: 10.3 MB (10295459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb142827615653e1ab4bf5cbcea0e6517c032af9197790b29ca0b79672e33ed1`  
		Last Modified: Mon, 07 Jul 2025 23:23:56 GMT  
		Size: 27.8 KB (27782 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:74d3c79d718a4d232470fe89248240661f6832f27c330452495a5250591f21e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301736865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a0297477e79f1d509bcb6d2492e2806ca853dc07cc39324329e397e09226c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600757b9c81e03e94454dc99e102eadb0af5caceda3e8c19007feb5ecae82656`  
		Last Modified: Tue, 08 Jul 2025 05:44:43 GMT  
		Size: 86.4 MB (86425424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93fe74c58f17b8638ab4c828f8d4b865821c43447e64c8cd4bfbde5a810c7b1`  
		Last Modified: Tue, 08 Jul 2025 05:43:08 GMT  
		Size: 79.1 MB (79051196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d100e50aeb7f571e7876199c2b01ed47aac5b8f1b65e84d6d897108299fe22cb`  
		Last Modified: Tue, 08 Jul 2025 04:42:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:d9ed33eb437de5eaf99e92cf9c3d1335528913fbbd555e26bfcdcbc5f4669e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10544411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d37de1bd49e141f4f6ddec3c36a34aa0991a9aa477b99baab6e3d0ef9a3bb3a`

```dockerfile
```

-	Layers:
	-	`sha256:d43c0e0b3556e7f94206feb35fc2fccf033c8b8d8cd13d50fcbea4324be5d72c`  
		Last Modified: Tue, 08 Jul 2025 05:23:43 GMT  
		Size: 10.5 MB (10516593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1272dcf2bced8af1694cf71b770c547711bbaf118c598ffac676d2736a3ae698`  
		Last Modified: Tue, 08 Jul 2025 05:23:43 GMT  
		Size: 27.8 KB (27818 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:204e117da43b8cf7af138c3c01cca20c89ab63dda3ca4cb76b4c51625bf57b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312154769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c7f47af8c31c75a35945a40b6597066b70b3fddb8309043a798e6210c32837`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c776d33dc276234326c920b797c5c9e8d471a1312f03aead5fa2529825185e6e`  
		Last Modified: Mon, 07 Jul 2025 21:09:05 GMT  
		Size: 89.8 MB (89774561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fd65ade23887bad8cc24159556378a6549464832612b1c87e5e65754cc9685`  
		Last Modified: Mon, 07 Jul 2025 21:08:46 GMT  
		Size: 81.8 MB (81820379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aee0ba4191b85c25bd6b403eb09e666ec500e916bd1906e335aa18ad2d3b47`  
		Last Modified: Mon, 07 Jul 2025 21:08:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:8c97d4faef33c0b63312e39738c123dcc8eb330d284fa0388eef7adc8464cdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10495939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556b9c47225f02a9e3b392e1bf05d1aba2bed380012647c74aad56e084dbe4d8`

```dockerfile
```

-	Layers:
	-	`sha256:1bd698a0a0e5b9790d9c07901bf4c2b440d507de1386b50b2ac06a12e881e792`  
		Last Modified: Mon, 07 Jul 2025 23:24:04 GMT  
		Size: 10.5 MB (10468323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd131b7c3aa90caf7e92e306c8397b766d59ae8e2a79db78327af10189e730d2`  
		Last Modified: Mon, 07 Jul 2025 23:24:05 GMT  
		Size: 27.6 KB (27616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:a3c09b820b834543ad816c80ef7f022109fac65d5af56094bba5bef96d275851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283448616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0c56f8375fe97412662b4b297e2d43add6ed42dc05e7dc666846eb526076a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99debc858569995ebc7f6d9290cbc19f540a471b716e06514603892b92705c6c`  
		Last Modified: Tue, 01 Jul 2025 01:14:35 GMT  
		Size: 48.8 MB (48775546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1158647b6db84897a383ed457f276b7c4d602a99d74b1c159bd2c138fd994fd1`  
		Last Modified: Tue, 01 Jul 2025 18:49:08 GMT  
		Size: 23.6 MB (23598851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3ea11d1e2f3faf8589ad741098f10976c65ebbdefe26521e25ec1f6abde856`  
		Last Modified: Wed, 02 Jul 2025 03:03:00 GMT  
		Size: 63.3 MB (63308526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490218841cb4006ccea3788c2da907c733bc1f20eaff61ff40fda60e6510af0a`  
		Last Modified: Mon, 07 Jul 2025 22:51:57 GMT  
		Size: 69.9 MB (69945605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd583f32ad8ca5ce8f1af178a35eaaa1ac5bb073d6c7ffcf91876ea3497aa673`  
		Last Modified: Mon, 07 Jul 2025 22:51:56 GMT  
		Size: 77.8 MB (77819930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93524b60d8f8f3eb2b058dfc0594d0729b8a88947ce54bebff0b2177ce067d0`  
		Last Modified: Mon, 07 Jul 2025 22:51:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:651e3d537b86bee4e3e678b08630ab80047b903bcfe8e9ad14ad67dee5019289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fc00e204adf1385fbee52ea09005bbe03e0da6bc111dddf266e59535663b9f`

```dockerfile
```

-	Layers:
	-	`sha256:01efb5c15576482e145575f503b45500e9c04c059249c304a040c7050c7c06e4`  
		Last Modified: Mon, 07 Jul 2025 23:24:11 GMT  
		Size: 27.5 KB (27530 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:1c4d90f4f63ad1187a609276dbbf49c13f0879493d54ba69db76f79b0f3ae3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318569515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36027028c1b8438d14d731324981f3166ba8282b5f70520e14196ba9d23feab4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57d9349410a306544d8415703fe52cf359c3239d46bb47a0ff96b2173c5c707`  
		Last Modified: Tue, 08 Jul 2025 00:33:30 GMT  
		Size: 90.4 MB (90369347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22b55aa5c49337c93ecd39f723f408177c4f428404ab6858571184b51126cd1`  
		Last Modified: Tue, 08 Jul 2025 00:16:14 GMT  
		Size: 80.4 MB (80359086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54eb7d45cbb167d99a9f75c90fbfeb3c8cc33e3b7f605f80880b4828c057841`  
		Last Modified: Mon, 07 Jul 2025 23:03:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:91aa7f54fb234af7bedf94c069589827845000b325a3263c493612d3e7fdbe7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10488945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9947c262af7dbfcde37061a0e3808b9c296048b1667069fdb593159e391732`

```dockerfile
```

-	Layers:
	-	`sha256:315aedafbab5885c9c0f3ea9223d68e2f23803d92a0b54d6735189241c7ce4dc`  
		Last Modified: Mon, 07 Jul 2025 23:24:15 GMT  
		Size: 10.5 MB (10461228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1df3f224440a088741b7f9973f581c307e5238de2b9039be67c846661064167`  
		Last Modified: Mon, 07 Jul 2025 23:24:16 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:be9439aef32b84c67f51a9a5cc220b46ad2e8e007beb5e9d7f67a250bcf7fbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49137d93405d2ffeacd84ae881007a5171ea621c07402ab08e5a234e05db42c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c580e287c9c366a32f1f5f19f852bd00d4ee67c95b7a4b3e443b2e65c5cccd97`  
		Last Modified: Mon, 07 Jul 2025 21:28:53 GMT  
		Size: 69.0 MB (68957938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff319e613d7718d33c97b2a4d68807464c2ed71607411d5eaa89b10ec085d5d5`  
		Last Modified: Mon, 07 Jul 2025 21:28:58 GMT  
		Size: 81.6 MB (81597964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1668e195dc57bea76e011a3a6b8ab02b1814c7703831647ec5fa3c3b5e6b6d`  
		Last Modified: Mon, 07 Jul 2025 21:28:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:c8332d9a3e328312a5522de52c81eed9eaaac5196be3de955191eaedc8ead6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1c07966c472b639023da1d2535d4a8f97304d78c2f443b97bf33ffdd328c6`

```dockerfile
```

-	Layers:
	-	`sha256:35fef79c4303aa4e1e775152295fc2ae8a63c9f120e1099469f08d1f35fd80c1`  
		Last Modified: Mon, 07 Jul 2025 23:24:23 GMT  
		Size: 10.3 MB (10320503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44cf62b565fe9819d449f55707cf97f82a26c6067b58a9fd9862eb845d296620`  
		Last Modified: Mon, 07 Jul 2025 23:24:24 GMT  
		Size: 27.7 KB (27657 bytes)  
		MIME: application/vnd.in-toto+json
