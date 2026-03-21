## `golang:tip-20260314-trixie`

```console
$ docker pull golang@sha256:228f4482d098aa716cc93d95ca92dbaab62e050b5a87ec0e800b8b828ef50592
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

### `golang:tip-20260314-trixie` - linux; amd64

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

### `golang:tip-20260314-trixie` - unknown; unknown

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

### `golang:tip-20260314-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:a8e0a052bcfc86e170d0e23f40d46c458ba378e162a48766e8fb71a8557b8591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294727569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24dbcca64d449ffca85f8e97e61cb9f7a0eca20c46ea82a496690e0e1aeffe4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:21:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 03:24:29 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 03:24:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:24:29 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 03:24:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 03:24:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cceb46da040530c459a3d55c1b9d0ccf68be7e284352029649a82437d5fc663`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 23.6 MB (23637012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e536a24ef93e50bf0d2984c667c771026334af7e30ed6318f85d146e4ff7a306`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 62.7 MB (62713901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bff02fd3494a14ae3f31b16c40b9133a57b9fd2462544da2146ff4422d71972`  
		Last Modified: Tue, 17 Mar 2026 03:24:55 GMT  
		Size: 72.8 MB (72805082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3549b40c9d6609f7ae376dd04fb2e1ccc5bd7d54b10023e8efe518db570d9`  
		Last Modified: Mon, 16 Mar 2026 18:06:19 GMT  
		Size: 89.8 MB (89838768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a50ba2e7c9b61b64c06513fba41e4464a331ef8ac8c2c71ebef3af96a66ed11`  
		Last Modified: Tue, 17 Mar 2026 03:24:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9cf9f67fb8d822cfaa9ed3c625cf4779e91d5351b097652655fd510703c0c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13886055a40f669387a6ded3aeb427c4081eb6cb8ad8bee2d386f6f22f849f01`

```dockerfile
```

-	Layers:
	-	`sha256:02915bbf9bd21262028f1fb5f1baaa71068eabf2829dca548176dbe25166fdd2`  
		Last Modified: Tue, 17 Mar 2026 03:24:53 GMT  
		Size: 10.6 MB (10581546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6103c20b57c31c4e7455fbd68ab2ac96f979106b535f764bfe144eb237703c`  
		Last Modified: Tue, 17 Mar 2026 03:24:53 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-trixie` - linux; arm64 variant v8

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

### `golang:tip-20260314-trixie` - unknown; unknown

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

### `golang:tip-20260314-trixie` - linux; 386

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

### `golang:tip-20260314-trixie` - unknown; unknown

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

### `golang:tip-20260314-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:18acee432126cf351df0933a49083d484a3e8823a8909c9666b055ce63b1be26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336480999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90277bffe7df720508e0c349b69b6f527d68e693962c0cdc0d62ebdc298ca6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 08:42:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:42 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 13:10:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 13:10:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76fd6649d6d35f910f2df9456726122ef27f29bb48c2f6e7ffbc7d318e0c0f`  
		Last Modified: Tue, 17 Mar 2026 01:51:12 GMT  
		Size: 27.0 MB (27013391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e880a549306a0c27a7c0db6951a348b972ff41cbbc4c467d5d3c95c7797075`  
		Last Modified: Tue, 17 Mar 2026 06:06:09 GMT  
		Size: 73.0 MB (73033284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1ef0247ed38f7a4b7b7776f4f220241d718538977da0d861b980db4a8bf1f1`  
		Last Modified: Tue, 17 Mar 2026 08:43:26 GMT  
		Size: 92.9 MB (92869851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ba3f21f31dd88c9cf395edb0e30aca822e3dcde51bd5a6421a6f428d5671b`  
		Last Modified: Mon, 16 Mar 2026 18:06:39 GMT  
		Size: 90.4 MB (90445965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e69de0913e31c61d265ffc44890d86809415368136f6d84b1831111608ca77`  
		Last Modified: Tue, 17 Mar 2026 13:11:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:40da66e12948db91c8175130fd471d04208008dfebb6d01c54303412109b5fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd77294a39ee6c9e9cc3814dad4879b85243706b4a529b6e86f3b12fc54ecb1`

```dockerfile
```

-	Layers:
	-	`sha256:9bbb3ce5f9234edf82a93a1810e5e7623c04488190b818c62bf4f913bf1e1fdd`  
		Last Modified: Tue, 17 Mar 2026 13:11:16 GMT  
		Size: 10.8 MB (10781447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f4f25d3c00c53574954916c3f72543d75c80181c5ddd04b6bbd1d57d70a473`  
		Last Modified: Tue, 17 Mar 2026 13:11:16 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:510a7b72509c96f92b9126e8f1dc7d0737e02b78b15d03be641b97ab4bc57968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (361964466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e404df226c870b92e856760f00642d6a6ed782cc4880dc790068245a2baa60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 05:11:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 19 Mar 2026 05:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 21 Mar 2026 04:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Mar 2026 15:52:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 21 Mar 2026 15:52:51 GMT
ENV GOPATH=/go
# Sat, 21 Mar 2026 15:52:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Mar 2026 15:52:51 GMT
COPY /target/ / # buildkit
# Sat, 21 Mar 2026 15:53:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 21 Mar 2026 15:53:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d52d7ab982f4bfd5cfc38caa0eefe3bfddcb1b2f76f02a38e1b10725b762ee`  
		Last Modified: Wed, 18 Mar 2026 05:13:23 GMT  
		Size: 25.0 MB (24954925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc9a450c15c86147b6c308f2cb25a618ec75f2ab5a64203aa728b5e309ab137`  
		Last Modified: Thu, 19 Mar 2026 05:35:26 GMT  
		Size: 66.7 MB (66662504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9c3d8cb0eb3839f60f443c07c78a4e233d415f3d669a49057b1e5f1b8cb424`  
		Last Modified: Sat, 21 Mar 2026 05:03:52 GMT  
		Size: 131.7 MB (131650375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2540b408e98980f08989b2a443ee35cdf7da6f3b7310d46cd1e63b1f1b775094`  
		Last Modified: Mon, 16 Mar 2026 18:48:21 GMT  
		Size: 90.9 MB (90904175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7193af3fbf23831504bb73cecf18d6f3f1fc6cb04fda3646dc80ab5bdfd60d3f`  
		Last Modified: Sat, 21 Mar 2026 15:59:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:009b9d59a17515f5c4e56c6788e6ad25f9e829722eed903c9bdcb5f839a9e027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d5d59fafd06f99f95adde0d4583cbe2d71e503e31443dbc6f21d854828203c`

```dockerfile
```

-	Layers:
	-	`sha256:be62bc971e47ac9e625ea73d66be6066e000c37c7e32ce41cbe607faabccd2df`  
		Last Modified: Sat, 21 Mar 2026 15:59:29 GMT  
		Size: 10.9 MB (10855280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e78691f85ed2d50d85b10e1c65bd2736d806537dc883afc67eae70ddbafee823`  
		Last Modified: Sat, 21 Mar 2026 15:59:27 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-trixie` - linux; s390x

```console
$ docker pull golang@sha256:ee622a2f0c5eb6b065bd0057f8a719ea33070b0a8848837a78f92e0b7d4078e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313703888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1565bdf1b9c01b3eb776538053811d7695be5b5ee44f91d72195293ec0f49a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:34:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:06:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:20 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:20 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 06:45:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 06:45:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8371259f6819197ae08830e46db090d1aad241011f8c2483f8e3205359263dcd`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 26.8 MB (26803190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990bcd0cd48258f05a5e1da913e50e516d08ed7812badfbb9d8451ec894a6a6`  
		Last Modified: Tue, 17 Mar 2026 01:34:59 GMT  
		Size: 68.6 MB (68628445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ef9c353b5dd82a1cb9fded9dd759c8310de3544393e1282d6fdecf1892f5d`  
		Last Modified: Tue, 17 Mar 2026 02:25:48 GMT  
		Size: 76.0 MB (75981970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e78b174fccd5298debc49ecb6092c7b356413921318c225406833e6427b55a`  
		Last Modified: Mon, 16 Mar 2026 18:06:51 GMT  
		Size: 92.9 MB (92925352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb03498544f28c47f6df0d12c3251ca95805e111ffe98b9bc3d2bf9d9b52dbb`  
		Last Modified: Tue, 17 Mar 2026 06:47:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:fdc5973dc48cf4708e63e66a7a1af671b866cf0d0063347b9c9a352d5926584e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cb30008903ab784b844f5ee45e408d0c3bb200960fcd5534567ffa79a16480`

```dockerfile
```

-	Layers:
	-	`sha256:cc5b1bda0f9081edcc3606d74806c2418efe1cd25b2ef3c18367cc69cb5968e3`  
		Last Modified: Tue, 17 Mar 2026 06:47:14 GMT  
		Size: 10.6 MB (10596059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4725f2fac68f763e8267dc2e783d7a36a23dda31078abb8bbd3a9b9ea179eb58`  
		Last Modified: Tue, 17 Mar 2026 06:47:11 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
