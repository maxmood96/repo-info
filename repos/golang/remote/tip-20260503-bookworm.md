## `golang:tip-20260503-bookworm`

```console
$ docker pull golang@sha256:378038d5d9606fa02502379a9e054797e1f427436344a88ecbc9af1d59e44b7f
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
$ docker pull golang@sha256:25f596b42f8f0ab5338a138daf8b6308a8f937a040a8287f85940eab4003ce3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326946611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef67b15757e02aa5b0259055cebd93b5ad6a7e493cc468780628740a4d1d1b1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:16:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:18:40 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 22:18:40 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 22:18:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:18:40 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 22:18:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 22:18:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb2acb8d415050c30a252376b24fdb59b4a191544712421ac38684c9cabae7`  
		Last Modified: Fri, 08 May 2026 22:19:09 GMT  
		Size: 92.5 MB (92479752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32be2e0f5add9aa550a86f2638e1a5bddb598fef09f796f2626b736ae1c11c9`  
		Last Modified: Tue, 05 May 2026 23:04:31 GMT  
		Size: 97.5 MB (97538809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407412e9629f4f04cc5343a1c0f194fd545edf5be0aaa6e236c4505f2cf2b1fe`  
		Last Modified: Fri, 08 May 2026 22:19:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f07be845a0c4c96cd6accbcfd33abf4fa5978da9ab9f6aec154eb8fa55b3b042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc249b157eefe9b5d2b5b8a70c0b6aa6d9fab89077cabc2ededf75160ee42e7e`

```dockerfile
```

-	Layers:
	-	`sha256:af0f7d7f610c4c8273aa6b6a455e24216acfbbe6d757ed2917441f53086eeda6`  
		Last Modified: Fri, 08 May 2026 22:19:07 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5864a58ec46d975badfbcfe71c06297306207351dad3a1f852b0e7e4a7a3c7`  
		Last Modified: Fri, 08 May 2026 22:19:06 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:7c4db321a2112f2b9c9a016172227aac31dc49cf5499e9d562f85d6fe24d770e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285529013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f7c200ff805a9b5db197db6a8eabef229f42c46662a592050f9126ec0c2ec0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:01:02 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 23:01:02 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 23:01:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 23:01:02 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 23:01:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 23:01:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef2e4eed112ac2d8730e2603fe97cab1d0ce708d52061992fd2f72e1db7e12`  
		Last Modified: Fri, 08 May 2026 21:35:07 GMT  
		Size: 59.7 MB (59653543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bff3657b1b239c54b2f6bbd5736b8eddc0fe0119673c4b3cf793020ffe1d97e`  
		Last Modified: Fri, 08 May 2026 22:14:31 GMT  
		Size: 66.3 MB (66342194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124712ceb426f7d5ea56fbdf12ab02ae56c25941c6892b6e8ce38b9f03ee67d`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 93.4 MB (93379030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247040705173b9f8ca201d4f6ac089fc0566f2e52112149ebc3e52ba0726def6`  
		Last Modified: Fri, 08 May 2026 23:01:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:30d138a4a0ef97e63790b8a5801a1acea694c05e665f38a48a8059afb188b304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8791b7d5129d806599c4a3c674fc1a97111a94e3bed25f0f631ba0a2ca2bb0e6`

```dockerfile
```

-	Layers:
	-	`sha256:aa4b4af2d7d1972ceb407c92f222e508b2660eef641ade86f34f02c1c26bc5f4`  
		Last Modified: Fri, 08 May 2026 23:01:28 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e6a09e1dce834f2caaa150f686f575e7ade09c840c4406cb05e19ea0c8ae7d`  
		Last Modified: Fri, 08 May 2026 23:01:27 GMT  
		Size: 28.5 KB (28497 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:96cc92499609715f31380172c40dbcb17bc94af5fcb4438eda600c25d32a64e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315260278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61924a744007d2b27fd07a9c64f5bb434560e93683a62a58563c45bb728a7a3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:16:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:18:09 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 22:18:09 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 22:18:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:18:09 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 22:18:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 22:18:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d254f77e845c1be8fb54fc989a5800337e6418b55fa06fec231b39daf9eba4`  
		Last Modified: Fri, 08 May 2026 22:18:37 GMT  
		Size: 86.6 MB (86555509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310d7048cbd083a777980fa032397ddcbb87e03b5b4b31ddec2b7fa305c5ce5`  
		Last Modified: Tue, 05 May 2026 23:04:45 GMT  
		Size: 92.2 MB (92242363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3eacf8e8d1af8f21c085ac7dff4de638a2cbd0d3cfa7c378c1bf26d8eaf359`  
		Last Modified: Fri, 08 May 2026 22:18:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:80512a4fdafed572b17a4efc8c95d375e81bf48543d093735aa9dfa031c54083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37961cb069b3483b35440755d1a148dab7a30cdddaff79bd30cb7318c60f4124`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6d71fcc507ccd69b2cb7ebebdeca149857c263fff60b850ddbe953df6aea1`  
		Last Modified: Fri, 08 May 2026 22:18:35 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c86cd7f17ce8eccc9cf95e0aed48ca32acccc3634c2f3f20f060f578cadff18`  
		Last Modified: Fri, 08 May 2026 22:18:35 GMT  
		Size: 28.5 KB (28522 bytes)  
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
$ docker pull golang@sha256:f58fd56861ddb600146dac14f8e933ee834c12baebc8af0fa1cc6c7caa18649d
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
$ docker pull golang@sha256:d31c4b26e322fe383d61e8efb7cc12b0d516d15db376c4989c215a149328e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec249e444b94061b25a019f1a0da6da59880209cb9bd54824d021aab7470a55`

```dockerfile
```

-	Layers:
	-	`sha256:661116b0e78b007b31e8d05719d539c5614096b7b9bf121b0a299031454f4cea`  
		Last Modified: Thu, 07 May 2026 21:11:51 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:5928e6091d147f0f89debaf848c21aaa1d17027eb3de0cf2264fdf948efa135c
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
$ docker pull golang@sha256:bca3137d285bb9f37eda7bd4162393be9f8fbc76447fcf5e6f5d7d505660f1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb9a8a991f11b64febc33a4f566d0a50ece701cf035583ee0b46876428cab14`

```dockerfile
```

-	Layers:
	-	`sha256:7bfd2324e5ee8fdc552e40d150f99adf9a1ac5064fdcfe10c27bba3a56ef5820`  
		Last Modified: Thu, 07 May 2026 21:33:49 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ac8803bd09b8c4c97c14d3da8182b43a76d6344549bce419517246171986c7`  
		Last Modified: Thu, 07 May 2026 21:33:49 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:f4408b6c9f1ba8349176cd02a7fe25d0362cc0967dc95ce99defa759a69c2139
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
$ docker pull golang@sha256:79c00a58745d3e6276ad2e5e5c022a92caa17130fd97400ee37c421c6b9f44fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1f059f457744f7e62ef77cc09ae1a825202e1cd3a360c66b11a4a19c575a0e`

```dockerfile
```

-	Layers:
	-	`sha256:a234272a5668cc345fc00df83edc258edbc8983725097a7c4a6b7d26eb895e18`  
		Last Modified: Thu, 07 May 2026 20:09:47 GMT  
		Size: 10.3 MB (10329539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ae4e16eea6fe2b8740b071c2cd6b44312a775c8a63a85074e6751d65cc1999`  
		Last Modified: Thu, 07 May 2026 20:09:47 GMT  
		Size: 28.4 KB (28385 bytes)  
		MIME: application/vnd.in-toto+json
