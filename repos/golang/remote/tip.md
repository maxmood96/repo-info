## `golang:tip`

```console
$ docker pull golang@sha256:8f920ad0c2fc9a14c829367685fb6a195ae4356cf9d1438df0e082486b2a4441
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
$ docker pull golang@sha256:521404a27e8ab92f19b4bac877209e79f008c4eab98731e8232d7aeca79c92a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338597380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2682ed0866aac77b1d89b5ba2f32a0db7519c4219d23bb573db4a779009e6662`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:27:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:28:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 01:28:38 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 01:28:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:28:38 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 01:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 01:28:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cb484591702aa3ed1d96027b72d23b12955d4ed3356e633bde95fbfab51bd`  
		Last Modified: Tue, 17 Mar 2026 01:29:05 GMT  
		Size: 102.2 MB (102170149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4384ef542a16608e9b825ddf3c86dc09e4324c50fc9718c0261655531fdcaac`  
		Last Modified: Mon, 16 Mar 2026 18:05:32 GMT  
		Size: 93.7 MB (93727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd11db966deac56c1e15fa279e9d47fe4888910a4423362ea2f0a312578552e`  
		Last Modified: Tue, 17 Mar 2026 01:29:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:d7a9c3e9eb2a844428c43c41fd46a41c6cc8cda0afbfde2cb306818776ef5ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6611f54839abd6bd46b55243270d1504d6bb2bd608ac47df5c28b0278a6f5b`

```dockerfile
```

-	Layers:
	-	`sha256:48fad71d443f19d21f2768002af266cf6d1df2235c60049e7704da4cf38a45b2`  
		Last Modified: Tue, 17 Mar 2026 01:29:02 GMT  
		Size: 10.8 MB (10785659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98aa4c8dd39fc537e2b971af02502c8ea5628891e13ae3efbf181766df9bc1ba`  
		Last Modified: Tue, 17 Mar 2026 01:29:01 GMT  
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
$ docker pull golang@sha256:4ea4fa29b5b681920d78a75c78fbcde4b1d912617ff2db7df2d378632fd646fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329496843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b8485fa46d508babecaafaa0e92a98cba0f5cc320f229a1d2f798de29a58f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:29:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:30:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 01:30:58 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 01:30:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:30:58 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 01:31:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 01:31:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e53e625ac21b3d881813126359002f787408fb50515a5400c639f9b986b433a`  
		Last Modified: Tue, 17 Mar 2026 01:31:25 GMT  
		Size: 98.3 MB (98309971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad36eab247615030277063307261e70ef31ab1fb10cb9e2a3d5ec600c3c4c21e`  
		Last Modified: Mon, 16 Mar 2026 18:05:21 GMT  
		Size: 88.9 MB (88913464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541665365bf65566c4a7bf11fc2d34d033826c880d7d31a246fd7a658c4b52b`  
		Last Modified: Tue, 17 Mar 2026 01:31:23 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:5340e614546a9621deed0f8907ce31bd6fb9f03f429546e777b12512dabc22d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62dbe5f2ae400e1d861d7552a6fdd9976df734c7711bee7197c02533dc2684c3`

```dockerfile
```

-	Layers:
	-	`sha256:6ef4e530e6b8dad3dedd47f35f00b63bfc7ca06edab96aa9b1e0580b9135dc16`  
		Last Modified: Tue, 17 Mar 2026 01:31:23 GMT  
		Size: 10.9 MB (10906114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b166acdd5a80420f1b5a52c81abba6397cf180f3a24e30de600a3145dea11a7`  
		Last Modified: Tue, 17 Mar 2026 01:31:23 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:b4e9258512f7089c4b62a8f9ba3ad9408de29f8f5ce65429be40076b6f92c607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339583437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af53d059ce95e05944ebc054cea3de725cdfc5201db1d3fa707b2ece164b837`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:18:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 01:18:01 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 01:18:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:18:01 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 01:18:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 01:18:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2aaf35fd2a2c9adf573b12a548dde1e9e6733b0a9d987c465038a81dcb2`  
		Last Modified: Mon, 16 Mar 2026 22:44:31 GMT  
		Size: 26.8 MB (26783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd35fd6ac345d92e539dc7dc49dc31742923ebf394762120d349ae52e655e6ff`  
		Last Modified: Mon, 16 Mar 2026 23:42:21 GMT  
		Size: 69.8 MB (69795316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa14c8a9badd0197f7aed4e22a959181c5af5864ff1a3279ced23be2b79e8108`  
		Last Modified: Tue, 17 Mar 2026 01:18:31 GMT  
		Size: 100.6 MB (100609122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beadfccec3ab6ced574e10800119a7f79c633318e3fc8b60061f1b218729af5`  
		Last Modified: Mon, 16 Mar 2026 18:05:47 GMT  
		Size: 91.6 MB (91576509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66e10730efde81ea1c5dc06671ae355db3007b630fc3d6d0addc56f5495c1db`  
		Last Modified: Tue, 17 Mar 2026 01:18:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:c10f5edf39d5c984bd36cc96d920cd25bebfa46f7d8d6c029fa022e2e9ca91be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5143083c4fe9d3c2b1d95602eba3e2387b3d2397cfaf7e710bf46e6c0a96a1cd`

```dockerfile
```

-	Layers:
	-	`sha256:6665acb0ee4f16adf33c514ce418060c1c50fdd84cd920afcdd71026ad5fd8c9`  
		Last Modified: Tue, 17 Mar 2026 01:18:29 GMT  
		Size: 10.8 MB (10756922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d33e63f0e917460244d04c0a7b8f9f5154f63c89201e75676f2bc034bd72e4`  
		Last Modified: Tue, 17 Mar 2026 01:18:28 GMT  
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
