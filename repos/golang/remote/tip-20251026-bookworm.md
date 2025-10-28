## `golang:tip-20251026-bookworm`

```console
$ docker pull golang@sha256:12e92dab179b21f11d377a592e1e0d5f66c0815c9ff7a4f1875cbe164ac16b22
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

### `golang:tip-20251026-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:53140396b68f27acc371268f2273ff4d86bcc0c155ee0c35d5c71c17ac9645ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320905479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff73273b8aac0b2e78421ce24c25ac1398df0d7ca5da2cffac12c9f900741d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f63fc01baa6c27727295945689d3665a62de85efe52cfceeea4873bb53f933b`  
		Last Modified: Mon, 27 Oct 2025 21:08:24 GMT  
		Size: 92.4 MB (92401915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed0125ec0f9fecb5ad10be0dd03e9fbc038a3da639715455b9acfe33ee37f3`  
		Last Modified: Mon, 27 Oct 2025 21:07:41 GMT  
		Size: 91.6 MB (91597540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08cad2ea6d053dbb09a81e19713b5f4e6f2ae4ce678a8bb2bdac8786d729412`  
		Last Modified: Mon, 27 Oct 2025 21:08:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251026-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a88a275fbe09b5d8ce67b1e775391c94bdae913fa879ca00acfa7f1e238a120a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2139c36912b68fe40381f4f1ff0d457b6d3435f724651ce028986922121ec358`

```dockerfile
```

-	Layers:
	-	`sha256:9c1716018a1bdafe3f4144c02d28bb0c290f21807846fa5b0d743f177c8d6c30`  
		Last Modified: Mon, 27 Oct 2025 23:24:40 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5802bb404a9bc3f7685889ff1c2a04d9a4c81626552c5d0d4401dfc006776807`  
		Last Modified: Mon, 27 Oct 2025 23:24:41 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251026-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:2f935eacbdb3d3f2427e613b0d1fba5fa0b9fb287ad9f9bf3a117b5083d2dd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279957590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5943c3339608a2742eab87d913aada150a26696b88fdbe8845dc3fbbf348e7d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4196186e4dcc2c499034efe9121e3ed26d36d9de3be01a984455db30c279ec`  
		Last Modified: Mon, 27 Oct 2025 21:11:34 GMT  
		Size: 66.3 MB (66255011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e78bce73be399b5f32cb65e0bc936590deb899ee136e761115443ad3660df`  
		Last Modified: Mon, 27 Oct 2025 21:11:33 GMT  
		Size: 87.9 MB (87919319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20cfacf9837ae2b4de75ab03ee790e47bddc03b18633a078c64ef2a28136d4a`  
		Last Modified: Mon, 27 Oct 2025 21:11:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251026-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fa718da3a2daf0a3a77e703295f360c6f809493387abd0533e07ca254df71734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6438aea2552e97f6e5809a9de9054d45502eda3688674b26354914faf2f08a6d`

```dockerfile
```

-	Layers:
	-	`sha256:8300ca6966c198ad1c29e2ad90635d0c3fcf9a6815836534789197765e608175`  
		Last Modified: Mon, 27 Oct 2025 23:24:52 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c2409218a9b6dcfb07b58a709c29f808f7ac669196b928ddddc4062f92009d`  
		Last Modified: Mon, 27 Oct 2025 23:24:53 GMT  
		Size: 28.5 KB (28541 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251026-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5b246ff2ce8970ec6bdf349b088334899106241c83edcf8176c23b08e4cdeff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309655366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14362098a437c80d082cf0d23b7258a636af9b7b1b5d1be00319e4b6a7297a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3c5184ee8e7cd4b3bfe4574d2cb60fac484abb3f2c3fbae196711c34043d27`  
		Last Modified: Mon, 27 Oct 2025 21:07:55 GMT  
		Size: 86.5 MB (86471658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75eb2c973c6fbfd8ad3a7e393b43c7170aa83e9a02eff9c12f176ce891587b5`  
		Last Modified: Mon, 27 Oct 2025 21:07:46 GMT  
		Size: 86.9 MB (86855633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a853dbdd686d2d6f582eb5143542897a6a4be9c607d8e62af5e94a9603f2e098`  
		Last Modified: Mon, 27 Oct 2025 21:07:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251026-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2827fde002b42a328507bde1e8b2e5bc5f5012ddefdbd9edcbdef9addecb3583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45c6a91c24294a27815084a35c7b952020e5b379140c94c14ec0ed6d75b4ef3`

```dockerfile
```

-	Layers:
	-	`sha256:189a5144479b3871690c3866e39f3ee47319887773cfbac463785350cb1701ff`  
		Last Modified: Mon, 27 Oct 2025 23:25:00 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba163f8d5666039c15b9189c7d8de77bd6d5746a177e1c31d2d0d3b18976380`  
		Last Modified: Mon, 27 Oct 2025 23:25:01 GMT  
		Size: 28.6 KB (28564 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251026-bookworm` - linux; 386

```console
$ docker pull golang@sha256:23b0f39223ff77f7ef835149ba01662f65a9d9e3dc7c55deeda0104734abedc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320132194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b18ebac32f850b5e668c7ffeba16364a2c29eba9d526b544ffe5892ae3bfc3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a422cf38caaa49217db814fb52afdb39103dacf35575ac5be7cb65c9c10aad6`  
		Last Modified: Mon, 27 Oct 2025 21:09:24 GMT  
		Size: 89.8 MB (89823285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306627769a351c52d3a3779e00eff7152c4e91ea12a59e21b051f7345636c1ed`  
		Last Modified: Mon, 27 Oct 2025 21:08:46 GMT  
		Size: 89.7 MB (89745922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c23efe1d51de2b02164f5fe829b237b01cd641b1230200e0b68f794c674f63`  
		Last Modified: Mon, 27 Oct 2025 21:09:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251026-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8eb63c097afb701b981c754a7925b4d0e823e2181f978974dcf07974c17ead58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba5eb124c3d54f4b43f85752d682cdd07629fac125622207ae0ddc9f4062958`

```dockerfile
```

-	Layers:
	-	`sha256:20698123b83faf94b997d350e998cf6758b0a58f100608578e832305848ca6bd`  
		Last Modified: Mon, 27 Oct 2025 23:25:09 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ae7856bc2c31679a54474384e721d3e6b3b57c09b96d901c39384bbccd5e7f`  
		Last Modified: Mon, 27 Oct 2025 23:25:10 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251026-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:48a7ec23f04c36f6da4bceef44d7b38ecd15f4fe8c3de6d1b7b9b62d870650f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291187039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4169563db7a273f5ba4c69ec7efaf0b53d7fbb597af1943689739809f73fde78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eca72dd31bb50cadfd79b7ad12f89f5688c744f6a098004e516ee38f52407c`  
		Last Modified: Tue, 21 Oct 2025 23:43:20 GMT  
		Size: 63.3 MB (63309417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b8b987535d1ca746e1df1d7a5e1bbbe17811a45d2a394c4b90bfa962bb4cb`  
		Last Modified: Wed, 22 Oct 2025 01:07:48 GMT  
		Size: 70.0 MB (69997127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53512436a1e8605814fc8630148c2ddfee921d5b88ff89a63ebb45d367fc91`  
		Last Modified: Mon, 27 Oct 2025 21:25:43 GMT  
		Size: 85.5 MB (85505793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43316fe891a97f8a662d35528b94cf57ceabe83c6f1df8fef6ed1517e706e4bc`  
		Last Modified: Mon, 27 Oct 2025 21:25:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251026-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:021d6a238acfc025a54117b2cd0336e92f8174ae4e494d6e8ac0033019bffb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 KB (28283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90430b2e6e0504571805d3690b3c0564ba0d7bb2b4ed8f24b7e2124f2821511`

```dockerfile
```

-	Layers:
	-	`sha256:b31ebb7be8901a8f7f82175c372a4138032a889ec5a6b50345b5344cfff41ead`  
		Last Modified: Mon, 27 Oct 2025 23:25:17 GMT  
		Size: 28.3 KB (28283 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251026-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:b89c4f137844ef3909e89f2d8bd625fb517d8dc1402579cc20e415800afb5cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.5 MB (326496819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1527bdcce5bc5d45d32ee199842da1ae50d0a1f7e13583df118baf3a853d99c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9014e4879ede8e5983b7a1a0f265054143b5d897d5a848c01fe4c938fdaa27`  
		Last Modified: Tue, 21 Oct 2025 17:30:59 GMT  
		Size: 69.8 MB (69845634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bdacc7744170991b6e3ec786cf581f2480e153c22dfc33bb6dd0e55bd8cf4a`  
		Last Modified: Tue, 21 Oct 2025 23:18:18 GMT  
		Size: 90.4 MB (90417857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f672a68eba01ff6a61528f0b4d6424e083bf2d654ca12da312b3edc3a8b90`  
		Last Modified: Mon, 27 Oct 2025 21:08:47 GMT  
		Size: 88.2 MB (88234264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd54f778d904387e63637453921cd79b2db662e23f9a96b6987c4d0226580489`  
		Last Modified: Mon, 27 Oct 2025 21:12:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251026-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5df4a6e6cca3a7fcf4f08cec0597483e2e1d13a31b2e871913608d53e569b705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7454c180550159fd3d050bfb79eb20b04c13d45251f6eebdc3b9eff75e88e73c`

```dockerfile
```

-	Layers:
	-	`sha256:99a713ab723ebe1b4377c46f3b62931adff18251aa4a2138e7eb65664307ceba`  
		Last Modified: Mon, 27 Oct 2025 23:25:21 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67028ed938adc205fba6af357e7e2fbbd57971c451c4b3108bff6d020b904a66`  
		Last Modified: Mon, 27 Oct 2025 23:25:22 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251026-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:9067e94c718197c6477588048620c626433ebd717757b42d33e79531eb38ca03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293488191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dfaff0e3943935d2efb9b82ee8e20672189296ddb3fcadc4ac4cb165e7611e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e5329ef731e263d1c6b30e55e66153c9c0292e1db1f30d716baf43f0fd397d`  
		Last Modified: Wed, 22 Oct 2025 10:22:25 GMT  
		Size: 69.0 MB (69006838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a092d1611329304bb10b51ed24c5eb7129e31e22cce2e99b258f719f86a22d0f`  
		Last Modified: Mon, 27 Oct 2025 21:08:13 GMT  
		Size: 89.8 MB (89814961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca43451135b0bf77490666837994d42444aaa96b13952b9440035828524936`  
		Last Modified: Mon, 27 Oct 2025 21:11:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251026-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cabdd8cb4b254eec99a7f9b05e4a3a0278375b17283d567f2babc107769db310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6ead344740e54c7f6703d7738f98736ba911a9c7c983e01d8e2acc2c4a049c`

```dockerfile
```

-	Layers:
	-	`sha256:8545289e6320e929132e15de12832e44bec0edef2b2db50c51e50436f6c3934d`  
		Last Modified: Mon, 27 Oct 2025 23:25:30 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f45eeefb5b448373515932544847a7c59866b52a7dcf90d09c90f5101a3a46fb`  
		Last Modified: Mon, 27 Oct 2025 23:25:31 GMT  
		Size: 28.4 KB (28428 bytes)  
		MIME: application/vnd.in-toto+json
