## `golang:tip`

```console
$ docker pull golang@sha256:77b1c351ac61ade4883d8b75860762df7f70bb833567a8a1c40f1ca5e394e830
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:914ff637fdebc0c024fa395a3041769a49a9a41074b6c706afa250388ad04673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345145660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b6d1c329e33431450b01c1d27cac5612d931b4c6b4a3206eb6a0bc287f4a3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 18:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:05:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:02 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:02 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:05:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:05:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4291833db4a83128807230cbdb61d2b25122323d71a5e3a4c8e44779ff71ebfd`  
		Last Modified: Mon, 16 Mar 2026 18:05:33 GMT  
		Size: 108.7 MB (108731774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4384ef542a16608e9b825ddf3c86dc09e4324c50fc9718c0261655531fdcaac`  
		Last Modified: Mon, 16 Mar 2026 18:05:32 GMT  
		Size: 93.7 MB (93727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd0fd28b615ea36efe9b4fbc3009023d2d2b3f3c4979fdf6c30610726211a55`  
		Last Modified: Mon, 16 Mar 2026 18:05:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6785a16dbb590916984d373beda77e3e43ac1c00a50b48c75e6262135e570a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c800a3ac67d262a72b37b1e54168bbeee2bc434916fda53c452b027c40701`

```dockerfile
```

-	Layers:
	-	`sha256:61e3e4a624ef1f5021dfa647af3033ca5e689da1de4641519feb7064535ae9a2`  
		Last Modified: Mon, 16 Mar 2026 18:05:29 GMT  
		Size: 10.8 MB (10785585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b0dc991f894812b1ca7ef7c5b85eea978e7f3beceb410c6cc76bedbe4fbaad`  
		Last Modified: Mon, 16 Mar 2026 18:05:28 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:300658e5b208bb413325eb5103c6ee8d2d63201f2e197cfcd7d74bbc39e5f5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300682560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344bd3bb593fd23253d217e59b89bb75a06d25713507c66831b5553343561672`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 18:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:05:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:53 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:53 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:05:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:05:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e7e4c87ce6959403c140ef3f01bab08f94d7dd517c0acf6ae810804957e70b9d`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 45.7 MB (45725086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77120a84626d4a7f2d6bdca75bb942d16ac419ff1bc25fc6e9d95035fe35f65e`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 23.6 MB (23633662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27016c2923c40df4d7f8b1909d8aac2050fedaaac6d29c1a4942dcab0ae038b`  
		Last Modified: Tue, 24 Feb 2026 21:35:13 GMT  
		Size: 62.7 MB (62713584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d5911a6bb299df3a88ad4462c9d8c1c8dd581356e490815be82d3aa4987d99`  
		Last Modified: Mon, 16 Mar 2026 18:06:22 GMT  
		Size: 78.8 MB (78771303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3549b40c9d6609f7ae376dd04fb2e1ccc5bd7d54b10023e8efe518db570d9`  
		Last Modified: Mon, 16 Mar 2026 18:06:19 GMT  
		Size: 89.8 MB (89838768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4e302b1419122542c39251483190ecfe40d3199d8db4c900438bdce58d2a54`  
		Last Modified: Mon, 16 Mar 2026 18:06:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:bc8b256b3262c21b49634a8f40d20c1bac46cffcd14e666f6ad169be9b5674bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cbc8ceae461fb6af0d85c4b10b808a12d9e015d8f9cbe1b903ceedc39a17d7`

```dockerfile
```

-	Layers:
	-	`sha256:be164a5ce14b33ce3301b707a8ca8546ac9b5176c51f1351e949daf7542d69d9`  
		Last Modified: Mon, 16 Mar 2026 18:06:19 GMT  
		Size: 10.6 MB (10581472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da561b01a944790554566740b4569fa7242bf411fa70906ee4be6845a19deeb1`  
		Last Modified: Mon, 16 Mar 2026 18:06:19 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6f5b10fd88144acfc9f6be61c87b9cdda6881e8995ef4ba64ad40ba5e6b1352e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927dda7f2c221df0d69728b9075564e2691193e2813dfc98c376aac62dcea06d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 18:03:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:04:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:04:51 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:04:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:04:51 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:04:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:04:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09ca43e1cee01c7f7a95f6e16e09168e7a19cf6214ffa79305167fc248bf0c`  
		Last Modified: Mon, 16 Mar 2026 18:05:22 GMT  
		Size: 104.9 MB (104917891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad36eab247615030277063307261e70ef31ab1fb10cb9e2a3d5ec600c3c4c21e`  
		Last Modified: Mon, 16 Mar 2026 18:05:21 GMT  
		Size: 88.9 MB (88913464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dba921116b327d82d645e06cd999ae86cc82a3e8cafeb220b68e54e47ad4f16`  
		Last Modified: Mon, 16 Mar 2026 18:05:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:9d7d44834c2813fe02f63d4c1f8ecae4dd0da6fc33d83af93da3b827739c26fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda1d674476058ae822def47892fa5d2a6e0419ea623ac68c80be368444a895c`

```dockerfile
```

-	Layers:
	-	`sha256:4b20364a434d50b1df10250329b88aea8854cd4148564289ff9f6eb21ed3b208`  
		Last Modified: Mon, 16 Mar 2026 18:05:19 GMT  
		Size: 10.9 MB (10906040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3918411232761a42f2372e47bbd13395e74921b0c35a4b87020c0e530274af1d`  
		Last Modified: Mon, 16 Mar 2026 18:05:18 GMT  
		Size: 29.1 KB (29128 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:aca7d7ee2f304cd5ae4eae2d4c9052df484271ebc468db2777795d46f0cd1a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345750491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb81afce0efc7f44057254a5cec8f22f7a944d90c53b9bc78a349e5d820978d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 18:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:05:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:18 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:18 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:05:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:05:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637225671ff7a033f6873454fdf6a539c15748206b024d30b37d32f91f3c21`  
		Last Modified: Tue, 24 Feb 2026 19:25:06 GMT  
		Size: 26.8 MB (26779652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c73fe9d5e539e615e830926d2ddb692fd4ffb36bb2ea42d3131dcab6528d49`  
		Last Modified: Tue, 24 Feb 2026 19:57:28 GMT  
		Size: 69.8 MB (69794855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b5c7731070d936c655b34ef48e5090030f8470d0157e2798ae0edda05e4ae0`  
		Last Modified: Mon, 16 Mar 2026 18:05:48 GMT  
		Size: 106.8 MB (106794045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beadfccec3ab6ced574e10800119a7f79c633318e3fc8b60061f1b218729af5`  
		Last Modified: Mon, 16 Mar 2026 18:05:47 GMT  
		Size: 91.6 MB (91576509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5704bdfedb754f7fa58fafb398f334c108951d3f0a2d3f941a8e8a895f1af`  
		Last Modified: Mon, 16 Mar 2026 18:05:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:e97788ec7068ac4f2080f5db841f026bdc94cf358450b05fd16556f4c4e6887f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888a737d165ae384157019b4ddf4b86d10f7cae4439fc138fd02d89fb407d021`

```dockerfile
```

-	Layers:
	-	`sha256:a94478f8ad76e4fc17a0476b9ac31ed9a907911bb16a6401469f39095849f296`  
		Last Modified: Mon, 16 Mar 2026 18:05:45 GMT  
		Size: 10.8 MB (10756848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf4b3b5b7fc2f7b0537adf819e9b3325f0481408b981fa784ef7665591ca0de`  
		Last Modified: Mon, 16 Mar 2026 18:05:44 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:5ded4fb60cc8426d7c00edd030cef9dabbd2b38c38a5728a5c64dd641085c4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336453019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa2559b2160040fec308f388c0d35445af562ad55282184df0dffed7c79ff87`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 01:10:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:42 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:05:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:05:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88c878e5079331d2b0e1bf13313604e6e446232728ee7b159499795ff9def2`  
		Last Modified: Tue, 24 Feb 2026 21:23:39 GMT  
		Size: 27.0 MB (27004375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078b8ed13f55a8d2e3bc098e87fe680e2a4289c11315d3e460db7bcd51cc93f`  
		Last Modified: Wed, 25 Feb 2026 02:59:03 GMT  
		Size: 73.0 MB (73022125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784245641f5583c22125d8b1795377396b0329cd3dddb9ca69cbe55bdfecb75d`  
		Last Modified: Fri, 06 Mar 2026 01:12:06 GMT  
		Size: 92.9 MB (92868135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ba3f21f31dd88c9cf395edb0e30aca822e3dcde51bd5a6421a6f428d5671b`  
		Last Modified: Mon, 16 Mar 2026 18:06:39 GMT  
		Size: 90.4 MB (90445965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43689c4dbd3be7aaa673816e7cd68a511ac3817adf011cca22445aa40e3b08c5`  
		Last Modified: Mon, 16 Mar 2026 18:06:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:c7a1bbd4ba0289caa33f46d00a2356054a64ce9c58e904d0bafa133b4517dad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef33e6f6918d27aa0cc73c016e833dab12f4b9ed098cd307550c38c0774b57d`

```dockerfile
```

-	Layers:
	-	`sha256:ade17f4836342d0f4c103abb2dcc0c4eca98c3b5b2fd6db7a676a7bf1410ad40`  
		Last Modified: Mon, 16 Mar 2026 18:06:37 GMT  
		Size: 10.8 MB (10781373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf1e80a47fea5b1e7ce6cb4f380fb83ef0b831abe6f8f639e79101b38bc4cc3a`  
		Last Modified: Mon, 16 Mar 2026 18:06:37 GMT  
		Size: 28.8 KB (28848 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:76c2dac96f02458845be87e88e3588c9258bf73837e0be2e149307fe3cc2cc9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.9 MB (361946052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9205882768f2d38b6579f2fdea0b26cc94c676ba909a86a34d034abeb7edd188`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Mar 2026 01:38:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:41:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:41:25 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:41:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:41:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:41:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:41:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c3a1cec8ab5f3346656c92bb6a04391222dacf945336ca2f360cb9afa1d32`  
		Last Modified: Thu, 26 Feb 2026 21:45:21 GMT  
		Size: 25.0 MB (24951819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1aad3c88d849328eee587bd71226c07edf0e2f5081fc7ec8dc66c3ee7e1d0c`  
		Last Modified: Sat, 28 Feb 2026 20:02:17 GMT  
		Size: 66.7 MB (66662373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37ae9709038f63e30e164a548c422deaa7a5733b337f89853b60db2fe5818b5`  
		Last Modified: Tue, 03 Mar 2026 01:47:15 GMT  
		Size: 131.7 MB (131650592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2540b408e98980f08989b2a443ee35cdf7da6f3b7310d46cd1e63b1f1b775094`  
		Last Modified: Mon, 16 Mar 2026 18:48:21 GMT  
		Size: 90.9 MB (90904175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7d87190be5bab2e5d007b5be2ab0c99868da35559a782d413ad34a49283840`  
		Last Modified: Mon, 16 Mar 2026 18:48:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6af0f541598a49f4e3a7e9c7be0e685cb25f032855e4a6c032a3a821d1bae394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f94c7f60e436d09be98910b889581cc233b49ff4c71cf565463ba3ecf8a11cf`

```dockerfile
```

-	Layers:
	-	`sha256:34ccdeff0ba1db1a3f8fc6f276688adc72e87a6c5f813090bcbc5bebf777a327`  
		Last Modified: Mon, 16 Mar 2026 18:48:08 GMT  
		Size: 10.9 MB (10855206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6fe9aeca77c4ac947587957ae209030642cb01bf2c16dee85a8166cd38a524`  
		Last Modified: Mon, 16 Mar 2026 18:48:05 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:52e5cff55e0c25e918634b04952cfec91aad4e93318b8583ff0546d28c525af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313685816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d312f8285aa500c05dfbf138e081a6f113ed8c77723564c6afecf42f19f1f8cd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:53:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 01:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:06:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:47 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:47 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:06:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:06:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b9712b896509afe6ce616cc91aa36b272afd379950384122674a69ff7d6929`  
		Last Modified: Tue, 24 Feb 2026 20:59:42 GMT  
		Size: 26.8 MB (26801071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62d9ba5f66f052b2790c9aa6ddd7ff161b24db86972e603be616bc922281de`  
		Last Modified: Tue, 24 Feb 2026 23:54:27 GMT  
		Size: 68.6 MB (68624526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9684e467c80be7a48b834eccb7a527228d490fb7acd8db34ebc728ce3079a9e`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 76.0 MB (75980176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ecba4cf50013ee6a115f596f3668950b1911ee32018b424bef2b193c207f45`  
		Last Modified: Mon, 16 Mar 2026 18:07:29 GMT  
		Size: 92.9 MB (92925351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b4b7f841fbf18e9125c468a368aa3d9b8673c3825dde4d0ab8e8b82e0b8107`  
		Last Modified: Mon, 16 Mar 2026 18:07:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:1f6053964d52940655ff31b4bd38ee325a8b07dd9b595cd415e3c8351c895f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b831e87bb5d3fb4e0ed01124ac105a0caf0777c587308fdd09d7b3da6e94b0e3`

```dockerfile
```

-	Layers:
	-	`sha256:99c44739c47acc39eceaf653b30e4eaf339c8457e54bc905805d06db443c630d`  
		Last Modified: Mon, 16 Mar 2026 18:07:27 GMT  
		Size: 10.6 MB (10595985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea4731063363f3e05f73816a4f9a52f338f75ec60fe2fd9c042fd4e6316212c`  
		Last Modified: Mon, 16 Mar 2026 18:07:27 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
