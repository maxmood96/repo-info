## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:97bb214191d76dfde9a135b60ba280babeb376e2a1442d18cb386b38005cf894
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
$ docker pull golang@sha256:21f25f922811d926e8eaf21c8b4b0323ca7de232824d9332a0260bd3599b0365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324391409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496ae98243144a3c70edfd646ad47fbe8a58ef23ee0d58d5a2015f616ef2ae02`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:05:03 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:03 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:03 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:05:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:05:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dde22db1863ca10cd9bbf88ceb1c2e0cca6082b8d10c571346be4198be8c95`  
		Last Modified: Mon, 12 Jan 2026 20:05:50 GMT  
		Size: 92.4 MB (92433172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e09070cc4c8c6b4577469e540a043174ece319f2134af5f8b6f76f4d7806aa`  
		Last Modified: Mon, 12 Jan 2026 20:05:02 GMT  
		Size: 95.1 MB (95051851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba7819a636ad71abed7becc2cfb517aaa851c7f08a6fa01a34bf7568fad5926`  
		Last Modified: Mon, 12 Jan 2026 20:05:40 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b9ccc406971841f05ad86eb70bb9e3d69bbe5d049e8ced17007f4da709871cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77df5e844e14a8f367a20c7471fcb7dad6027b0cc8febf49f18e445995b7a507`

```dockerfile
```

-	Layers:
	-	`sha256:ef156a9e3b53bb9d953ad4a82f51beb074ad9f8b0e80343462c8aec5467c13d9`  
		Last Modified: Mon, 12 Jan 2026 21:25:17 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbcb15ce9b2550bc58ffbab4e6da86d778f8aec8b19cb9786aec578d10b4f895`  
		Last Modified: Mon, 12 Jan 2026 21:25:18 GMT  
		Size: 28.4 KB (28385 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:9dd69be76074c3d2d7399d5cf1d1e19a55600e2465d479f853df41d064de2c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283206545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c848998be06062e19637bd13b48798edd85556534682dfe01b262a68991793`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:07:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:07:53 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:07:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:53 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:07:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:07:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f06489595662b32227ed4939431e5099ae83a2661a5770c752a389e68e400`  
		Last Modified: Tue, 30 Dec 2025 02:06:44 GMT  
		Size: 59.7 MB (59652384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc98fc7c621e14d0e6742f2184cfb67e65e411577d2485fec3e824a7040cfb3`  
		Last Modified: Mon, 12 Jan 2026 20:08:47 GMT  
		Size: 66.3 MB (66288717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb06c5933c094de46d52df9ed5d5962ecacceb10cdc72056e1307b0ee8c18640`  
		Last Modified: Mon, 12 Jan 2026 20:04:47 GMT  
		Size: 91.1 MB (91134394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345f68720b240cfb31363476f9d1fffc1d41c95a262797bf9066e6824140187d`  
		Last Modified: Mon, 12 Jan 2026 20:08:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e2c7396e974ee3e679b8255d08ad4e7a7c95cf921d106703beb254eb4b49cd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51cb3469baf5a002f31cea61de26f2ec4971c54cbaeaa3d6fbd9988ad66efa0`

```dockerfile
```

-	Layers:
	-	`sha256:551cc8ecb5073d9edb349675177816479d4189f844a5ea0b5c90327e52ed2752`  
		Last Modified: Mon, 12 Jan 2026 21:25:29 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7d27dcc81b184809c58ba9a6790e1793656ffd4a3758b2977a9de2a154a77c`  
		Last Modified: Mon, 12 Jan 2026 21:25:30 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:62ee3805bd00c49d81c2e5896eeaea37373d0f8135f18347836a3f41557079e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312972923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836967125fcaf7a63ca8ced3ee52c5bd600f7f8d244975a4728a3a60e40323bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:04:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:04:51 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:04:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:04:51 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:04:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:04:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7613ec890ee6f64aeca847e9e962cc46e1c39f91f6f4e3429289c78f76d96c`  
		Last Modified: Mon, 12 Jan 2026 20:05:35 GMT  
		Size: 86.5 MB (86506761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cab7771dc3fd9d6c93b2e8fcd20d3b05cdc987b52c3e09c78b1417acc8931f2`  
		Last Modified: Mon, 12 Jan 2026 20:04:26 GMT  
		Size: 90.1 MB (90137309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93deee77721af747f49673b8d4c1864ad05b948e2f9550f4440b35e4e41f821e`  
		Last Modified: Mon, 12 Jan 2026 20:05:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:719b30d90e4398706888a489a728bf4d17ebbc193277edb7c032779c22e38ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105cf71264a91b0c1b765074fb831564e7ee8612aab8d95e040a8f83d6736175`

```dockerfile
```

-	Layers:
	-	`sha256:c39f582920dd6dc55c62dd386281fbebadb09daa70e860849992167f82d38782`  
		Last Modified: Mon, 12 Jan 2026 21:25:40 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647ffce85f1b1f8cc7d544f23a0936d307b17d46608232008dfd5e5f026b69eb`  
		Last Modified: Mon, 12 Jan 2026 21:25:41 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:b07000718e52ac9eaff759a39edcc2bdba35a0df1eae3d72d9c4276ee75eb049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323369353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0a3877e3854a2042d0be976ecdea899222a8a76684504f93e446603855cc4b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:05:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:40 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:40 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:05:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:05:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63bb42155eb2fe3cb6496304c20382db95885b672da0e34a3fffa188861a6ec`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 24.9 MB (24864466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10eedb7d741cb151d52259302acf62c6c98590a9a4168d4370619e890f15715`  
		Last Modified: Tue, 30 Dec 2025 00:32:36 GMT  
		Size: 66.2 MB (66233282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca9969a643c82f016d64844f90f0937c6ee1b37d511595f7cb770b88bb5fb80`  
		Last Modified: Mon, 12 Jan 2026 20:06:21 GMT  
		Size: 89.9 MB (89859014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42b2997976651e9da981a359adb745663b505ba580ded35d1fcd67a84ec5f37`  
		Last Modified: Mon, 12 Jan 2026 20:05:45 GMT  
		Size: 92.9 MB (92945554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd39c5bcc04c760e20f493f384fdad629f42810b0fe2523cd9ff8265c3b1483`  
		Last Modified: Mon, 12 Jan 2026 20:06:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:796028350d09ff234626695c8f729a20bfa1320ec0cbcdd474873827be6be44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f334e754385693b34d74a498437f6c1d3adbb83517b4b6bc9b1e60a1aa9b14c`

```dockerfile
```

-	Layers:
	-	`sha256:602d6e7cb7173ed55daf1b8a5c212277fdeafc70385db06ea8fd7703a596fd12`  
		Last Modified: Mon, 12 Jan 2026 21:25:51 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc14e2399ef86c5fcfb2e5b43be71bcfbd4815bd2d4118faeeefdbc3535ccd8`  
		Last Modified: Mon, 12 Jan 2026 21:25:52 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:8389923f0f4ca7c206e7c1d69deb89378bfc20880bb3cd10f2a6b69e5336aa8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294510604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ff74b9ef73d44f829632144f6ec2abae1db156b1e2c17f2653d0b9fb10201`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 11:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 18:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:22:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:22:47 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:22:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:22:47 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:23:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:23:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a43d59f754c088126249c7de1413be451574eda24274414bef9aea85a3ac886`  
		Last Modified: Mon, 29 Dec 2025 22:38:14 GMT  
		Size: 48.8 MB (48760925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec26c7ec0c76b4716fe076707c8489ced71c06858c4f9f03f18c306cb4344cd`  
		Last Modified: Tue, 30 Dec 2025 11:50:06 GMT  
		Size: 23.6 MB (23613812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2269474ce0b0fca7a225e6021a034ce6b526a7a59bdba22d740e8cee0614ec`  
		Last Modified: Tue, 30 Dec 2025 17:14:42 GMT  
		Size: 63.3 MB (63309491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89852c6abaaf7d3796bc5819d2aedcaf5c64f4004295c9c5b5f990b11c07ba`  
		Last Modified: Tue, 30 Dec 2025 18:23:03 GMT  
		Size: 70.0 MB (70016959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a831f31f3ccc6903fefb1751e80553dde8e9c3ac9501ef429ef0c2121806bc98`  
		Last Modified: Mon, 12 Jan 2026 20:25:17 GMT  
		Size: 88.8 MB (88809259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c0a75bb4777652600df46c93da7678b8ae65a2c4ed72c1e83286bb0e7b790c`  
		Last Modified: Mon, 12 Jan 2026 20:25:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2b053cf570d7f83880d0962dcbf17ee7b7476523e408ed20c47e28f8cc6cc28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73eca29ffa102dd9dcdbd68b2260c16cf3d0d8c8cfff16e01194cd46a2767e8`

```dockerfile
```

-	Layers:
	-	`sha256:7d04c080019303bf736b6414743e287cc99fc578fd34315c3a5b656246b420f6`  
		Last Modified: Mon, 12 Jan 2026 21:26:01 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:de8ccd310ed5eed26b7b5a2fc0628862894054849c5bc5681af69fabd06533d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329948599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045a655f951a980f6d47931f3be4e514a2ae60d566043d9476c296147ea9d120`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:16:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 08:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:00 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:05:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:05:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7517c515ac5fd6799cec288b72512b8ea3fc54d2d37de5af54d06ba0ea2f21bf`  
		Last Modified: Tue, 30 Dec 2025 01:31:20 GMT  
		Size: 25.7 MB (25672165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ff2cfb691fedcba1692cb13fd0632001d1a876833f4cd2aa52eba87257a8f`  
		Last Modified: Tue, 30 Dec 2025 03:17:48 GMT  
		Size: 69.8 MB (69845530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb3fd09a1e6774e533a42b26351be92003f5bdea475b8caa70173ad58b79d9f`  
		Last Modified: Tue, 30 Dec 2025 08:43:16 GMT  
		Size: 90.4 MB (90419830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c1f34a163f68379a85adaf1396976b01cd79b6100ad42ff3e6581c97310f7b`  
		Last Modified: Mon, 12 Jan 2026 20:06:42 GMT  
		Size: 91.7 MB (91683920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba7819a636ad71abed7becc2cfb517aaa851c7f08a6fa01a34bf7568fad5926`  
		Last Modified: Mon, 12 Jan 2026 20:05:40 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b65a5c63282001f32ee106dcb7a4228116d709af63712a1aaef3645557058789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d42f656d58d6d0c711d84d2b76b84d0403bd2fbc537ed4a98c3e906e72578c`

```dockerfile
```

-	Layers:
	-	`sha256:bcfe82eb16619fa9188d628a0d5912b770372cb2e275b2d9371328b8aae476a4`  
		Last Modified: Mon, 12 Jan 2026 21:26:06 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8a6c4142dcddecbeb1421d1e9366c8b07cf5d0065748b84441e955dd26a249`  
		Last Modified: Mon, 12 Jan 2026 21:26:07 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7649acb2caa2430585f357819fea71e50c6de3c7f32e80d3e3a3bdae531fe9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297907031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa8cd64fb3f1bf0393261213c111bd1a746654a8cddddc8344e05864588751b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:19:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:19:09 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:19:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:19:09 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:19:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:19:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acc4c1479120c6249296b3550670caa7738ba389b23a7ca3973f7732c12c0ab`  
		Last Modified: Tue, 30 Dec 2025 00:42:34 GMT  
		Size: 24.0 MB (24027124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d337299523414af9c112b1b1a1d201a2c6eaec2baa26798cdadeeaf575ed2`  
		Last Modified: Tue, 30 Dec 2025 02:20:20 GMT  
		Size: 63.5 MB (63501425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cade7c11e2a384e856bb2917369c47ddecd37868c2ef72ed6042a2765c4308dc`  
		Last Modified: Mon, 05 Jan 2026 20:14:59 GMT  
		Size: 69.0 MB (69010692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c721b150b3efd4976a8fc9ccaf826512a0d88981fdddc7ad84ff81c3bfa69`  
		Last Modified: Mon, 12 Jan 2026 20:21:03 GMT  
		Size: 94.2 MB (94229904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4d53ea7b41f31103f69f94e440f8cbc0cd52474ac3cd07a9e06d1e1b7ef85e`  
		Last Modified: Mon, 12 Jan 2026 20:21:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:00519c01f565c62d45b6351d43231ab611bc0409922d6c3e3662f7143087e923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99953584771449734d007cab5676f0573564d94785705b8f13dd5ea0e258c3fe`

```dockerfile
```

-	Layers:
	-	`sha256:96cb7aba3ee74a2c132985fb7696af89cc329a0ec1bb1c057c6242eb72231873`  
		Last Modified: Mon, 12 Jan 2026 21:26:18 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede8099b4642c36e6d2007e00da1eae6fdf14b5e17e90f1544f3e4d59f3052a8`  
		Last Modified: Mon, 12 Jan 2026 21:26:19 GMT  
		Size: 28.2 KB (28212 bytes)  
		MIME: application/vnd.in-toto+json
