## `golang:tip-20260503-bookworm`

```console
$ docker pull golang@sha256:c17f2fdad66d1d49fa84f747f69b2e9ee0a79574537578ad27038a327e540a4c
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

### `golang:tip-20260503-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:c031b9c4950b75b40c7997f3189db026fa646ca9d49b6c47d182f701782983e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326946615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2102f12236671d36f2e4e136a8b988a8735eed8f35debaaca2214eeae677d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:45:43 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:45:43 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:45:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:45:43 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:45:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:45:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda2b4d7993820b00c5488d173051e76d01ba6b85620617ba77001b0f9e2fa`  
		Last Modified: Wed, 22 Apr 2026 05:12:28 GMT  
		Size: 64.4 MB (64396988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f86d8f2663dbd397c07b8a85126e33908c4624c95b80d3e0d9d3843a76100b`  
		Last Modified: Thu, 07 May 2026 17:46:13 GMT  
		Size: 92.5 MB (92479799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32be2e0f5add9aa550a86f2638e1a5bddb598fef09f796f2626b736ae1c11c9`  
		Last Modified: Tue, 05 May 2026 23:04:31 GMT  
		Size: 97.5 MB (97538809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9b82965df5960797383c9c7c7375251a6e9f1ca7e218addbcff81bce3830de`  
		Last Modified: Thu, 07 May 2026 17:46:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e06b87c78af47e179eddcb8caec80772d7a884c0b3d807354040bf538332677d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53f001ab5f15310930b910ac36332ef732eebab1aeb425a2311fe69e9e7e0e9`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f3f0aa8ddbd21cea860fc66bd1b11239921573efa047c06c1ee6aaca2e26`  
		Last Modified: Thu, 07 May 2026 17:46:11 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550d6a3b00239762b0bef333d06c8fe74a459724b30b3c4034df2aaf81f01fa3`  
		Last Modified: Thu, 07 May 2026 17:46:10 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:bd103f881c66d671be400b86a4935d3738386d70f6575a54147e49dc7fd09277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285528448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89119c2195e106121d42af653fd6326a7ddfc05f5eb9c8237c991fd1dc2e8a8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 18:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 18:19:52 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:19:52 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:19:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:19:52 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:19:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:19:54 GMT
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
	-	`sha256:72bc3298886fda47bf3ace35780c9aaa3df4cb447d294434850eafbc1b0e467d`  
		Last Modified: Thu, 07 May 2026 18:20:19 GMT  
		Size: 66.3 MB (66342405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124712ceb426f7d5ea56fbdf12ab02ae56c25941c6892b6e8ce38b9f03ee67d`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 93.4 MB (93379030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f59e980b1c73cc66461323dabef4d59b2f517e64b44074819862911aa09017`  
		Last Modified: Thu, 07 May 2026 18:20:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ec28c16024021bd9f94148c9f6505456b95dc3ee778a215712f79c2d35fb0ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b14e8995dedee1c18651c30c430c86e9a5d5a24990a81ae81f5f8e53e294178`

```dockerfile
```

-	Layers:
	-	`sha256:7c4b75e2e252ed874cd287f97ad423f87ee6331b48f3fa9348a984a0a0647a95`  
		Last Modified: Thu, 07 May 2026 18:20:18 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6fede686be002ca0cabac3b0366ce22e9ceef8c0e40d53c9f85ac922df14589`  
		Last Modified: Thu, 07 May 2026 18:20:17 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d5f47501477725838a92d1a92bad65d5bb06fbb83b0616e085eed00f2c5b23dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315260164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8abf36e1065213f0a868243209b6cabf3fb91449badbf66b21c74403553616e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:48:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:50:27 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:50:27 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:50:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:50:27 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:50:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:50:30 GMT
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
	-	`sha256:fb3a43b2227b0d2574de3633c5bab9226930d3ddea35caef932726b417a56cfd`  
		Last Modified: Thu, 07 May 2026 17:50:57 GMT  
		Size: 86.6 MB (86555543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310d7048cbd083a777980fa032397ddcbb87e03b5b4b31ddec2b7fa305c5ce5`  
		Last Modified: Tue, 05 May 2026 23:04:45 GMT  
		Size: 92.2 MB (92242363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657058f9935de93f875637fc69affee49e284a1360b637bc8a70fe44ec75863`  
		Last Modified: Thu, 07 May 2026 17:50:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f01f4349a3958c26b0590f616cb5219916024d47db357fd9649af46289d72cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7620395fcfc94d6e4c9b38dc99eb9bf304aeddee57c723d3979315430653ded6`

```dockerfile
```

-	Layers:
	-	`sha256:15dc354ee4089bfa096534e12cfbd10b89e73a1c6ffa28620ae1c799019869af`  
		Last Modified: Thu, 07 May 2026 17:50:54 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b73706d149610b822b15a20631a795e4daf6fbc848f9a368388c8fc78e67311`  
		Last Modified: Thu, 07 May 2026 17:50:53 GMT  
		Size: 28.5 KB (28520 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; 386

```console
$ docker pull golang@sha256:e8ef29078151216ec9fa06c9303c41276d2895c58cc659c5b4fc5c748ba730e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325769533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee04e48cc5d10a69b14c8b99a0f50bdc97de163c644a05c0718107eb03cee725`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:42:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:44:20 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:44:20 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:44:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:44:20 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:44:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:44:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d771f6f5a1356deff0c1540de8894e5249a2f8c97ba7961a41235129f48c60`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 24.9 MB (24875723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd81f3dc271c0572c6da562bcce13d5c0a8f379729949fde98b0b1e57ca2e4c`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 66.2 MB (66235084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd4c5c9d7712a95f7730838bf1018afd0d83771edb27c4e64ceef3bb615cd90`  
		Last Modified: Thu, 07 May 2026 17:44:50 GMT  
		Size: 89.9 MB (89901021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b12f480be5869cc9862686abcdcfb3464484b704815a3a70c6077d05037bb`  
		Last Modified: Tue, 05 May 2026 23:01:30 GMT  
		Size: 95.3 MB (95279830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524a47d94520347bb1e674467b0e1e9cd52e7520abc3b3ff6ca210ce2cb3daa8`  
		Last Modified: Thu, 07 May 2026 17:44:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:946568ee8d495f5cc89ec8962260d6a26336f2b45af2ea9a22da3ac6dc6146df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12d86884b37ad57f67d29e771930e82460ecd736246b0838f07208d62d61a72`

```dockerfile
```

-	Layers:
	-	`sha256:105cea63b6426265ea2fc68f10dac01d93e92d9d7c1422af2eefc56cdf7e094b`  
		Last Modified: Thu, 07 May 2026 17:44:47 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e280e3f593b672823f4072baeccf124d5fab1cd20bf9194b6c560584d3f05936`  
		Last Modified: Thu, 07 May 2026 17:44:47 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:18f426522435d2fd137837a3e4569ba34e401d03ebfc264a6fa0ebc88e3fca3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296915944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3e2d79e2fac1c871df72fdf71f0e6063a6d8f5cd6483eab7b603cd6f96e706`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 13:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 18:49:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 19:35:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 00:38:11 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 May 2026 00:38:11 GMT
ENV GOPATH=/go
# Wed, 06 May 2026 00:38:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:38:11 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 00:38:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 00:38:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d3be957b775aeb19be93537211a85a2a31f49a07f3bbc6044dcea43e1c8ad87b`  
		Last Modified: Wed, 22 Apr 2026 01:25:51 GMT  
		Size: 48.8 MB (48782445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689fafc394c7107b6f97558e80faf7c6aa5a2d625bf130259c59cbe1f85ed9fb`  
		Last Modified: Wed, 22 Apr 2026 13:39:30 GMT  
		Size: 23.6 MB (23615606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451e7b3cb9c9d1c48a12fd45433b4710af87bfecf6744a09df7916580c67c305`  
		Last Modified: Wed, 22 Apr 2026 18:50:27 GMT  
		Size: 63.3 MB (63309466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1d9d3dbe215b8bcf0455f627ea3048e9af9e774f3f36403e2e0c26f0767680`  
		Last Modified: Wed, 22 Apr 2026 19:37:24 GMT  
		Size: 70.1 MB (70051299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405d866fce40cf012a2813b4ec3f8ded62ee03eb789fadfdde1d73f1f403f7ab`  
		Last Modified: Wed, 06 May 2026 00:40:22 GMT  
		Size: 91.2 MB (91156971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f2a3e169b03852d7829afb798842f63aab027107a50c2fccfa9e4ea3a1e854`  
		Last Modified: Wed, 06 May 2026 00:40:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f498f2a442a65f41e62d5a422979f6974c203fcf8e2a183c6aa13d94158fbc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e076eb729164e9c9390c4148c167cd16a00bc0491e726a2e7116ca12a7b04`

```dockerfile
```

-	Layers:
	-	`sha256:3cb4dd3302fdbf8b387d33e8a889c05e5ba1e24b9e24c76da4a9a72b07e7f8f9`  
		Last Modified: Wed, 06 May 2026 00:40:11 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:75b552d9b78f7a511c96be5082613a2adbe68c3bed4e59e05d249cb9cdbeaef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.5 MB (332480214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18161bd8a0ceb9b129130030cdc92842970ebe11ea6e71e836debdbae7b7294f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:38:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:40:06 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:40:06 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:41:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:41:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c150273f4a5b502fcc97d9a922e79c7bc7d5035fb9eb1142f5adfbcea709a1`  
		Last Modified: Wed, 22 Apr 2026 03:39:23 GMT  
		Size: 25.7 MB (25679369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5543a629afcc86e06f307e20d98c8cdd9f2490908cdef00122fb2daf671594`  
		Last Modified: Wed, 22 Apr 2026 09:37:35 GMT  
		Size: 69.8 MB (69846406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1c452e78180d60e24977df1dcb4ebc1677454892dc72552b751eef112e143c`  
		Last Modified: Tue, 05 May 2026 23:42:40 GMT  
		Size: 90.5 MB (90488872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df66d548befa9f03e6fb22cc6385677d9c13ab71d11ae10a9cbc0d2e3d0efc16`  
		Last Modified: Tue, 05 May 2026 23:41:42 GMT  
		Size: 94.1 MB (94128677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38533b5ee47cd3e297878c91675e7359bc6842e903087cb39a0dab7e15a799a8`  
		Last Modified: Tue, 05 May 2026 23:42:37 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3bcd6fcba1c93d7398d5d9db2a7ac87014345cdf5c5e2118b8ad52a5724cd18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a77f7b8488d71833a58054836eaf2933c118b28aac3f9706de4e365d4b80f9`

```dockerfile
```

-	Layers:
	-	`sha256:903819062ea6904edae7691fab0efc73a73ef37846c0294cc2d462309f25a876`  
		Last Modified: Tue, 05 May 2026 23:42:37 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d410f8f0368043446c553c3d4827cc1771866febfdf955357b2d8807c8c6753`  
		Last Modified: Tue, 05 May 2026 23:42:37 GMT  
		Size: 28.3 KB (28258 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:d1e2a57c2c364a20b68680c3b24fd82c619222942b97bf52a91f6ac91d062b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 MB (299871901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0310902bcc5023ad13bd6357e76dde1c3d501d6d31d1864511b0565988dc2459`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:20:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:55:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:58:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:58:52 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:58:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:58:52 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:59:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:59:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac385f32c2d6e9209dd9f8ada378863aba00921ac3815f399e84f802ea5ce36e`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 24.0 MB (24036363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df5494ce4223646f47cc2e95923748571f15dc98fdcd0c46696a358fa2128f`  
		Last Modified: Wed, 22 Apr 2026 04:20:41 GMT  
		Size: 63.5 MB (63500148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191992e53cbb3a1e8f590d298a4aaebf2dbe6c1bc858f52108b54fa18b6e1d90`  
		Last Modified: Wed, 06 May 2026 00:00:24 GMT  
		Size: 69.1 MB (69081673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2604867f1d33ea36e2647b9da201fb796e01f541d58d01f7899b6b2cfc20d4`  
		Last Modified: Wed, 06 May 2026 00:00:26 GMT  
		Size: 96.1 MB (96105590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77a81733c2d36a2467544be10293816e06e3828f0052c661121075a796f0367`  
		Last Modified: Wed, 06 May 2026 00:00:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:dde8adc8df9e7bf0e504593839ac8eae6e12781b9238b3854c894de949bf1743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedb246c1207be9bdc1b815eebe65a676393669d8445cb0b1bd9742af64e9d88`

```dockerfile
```

-	Layers:
	-	`sha256:6b1036dca3ce2c8f2c97c49e67c6f73f12317fda58baf96f746791968bb48d45`  
		Last Modified: Wed, 06 May 2026 00:00:23 GMT  
		Size: 10.3 MB (10329539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40e8ea0609255f814e477765369f21be778f483a79b81f73ec4ab6291ff9bd6`  
		Last Modified: Wed, 06 May 2026 00:00:22 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
