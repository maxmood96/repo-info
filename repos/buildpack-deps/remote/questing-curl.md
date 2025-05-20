## `buildpack-deps:questing-curl`

```console
$ docker pull buildpack-deps@sha256:75778de0f72e6f744ed737d36ad23695067be035be6d0e971115415e9cbca38c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a6827ed16adac7341745ffe35d25cc44c5c9ed899def5830e6ba303553c802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49107875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e84267133968676ae14d746601fc2427e7221da3d2dfdee5a52862af42d9a85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:22:07 GMT
ARG RELEASE
# Wed, 14 May 2025 04:22:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:22:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:22:07 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:22:09 GMT
ADD file:3cec1fcccaf2006b6ff56dc605b2e64e601533472cc244b39a2b9bde0eb3c32c in / 
# Wed, 14 May 2025 04:22:09 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4b55e964632f88af45c8e80fb4c2f85a63df0f1dbb9104a9ad05b18c2f6e6e20`  
		Last Modified: Thu, 15 May 2025 20:04:43 GMT  
		Size: 29.3 MB (29281519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80815c365ceb18a92253949ab20996338ac263328afe74f7c1321666e7d3b111`  
		Last Modified: Mon, 19 May 2025 23:37:16 GMT  
		Size: 19.8 MB (19826356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13450eb2debfecdf74006a209f0e68d7e84bd738c40bafb01bda81fed14ce69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bd96fb3cbc38c27ab371e3bd3ced3be63a1247556b7ec5e352602c1663e2b3`

```dockerfile
```

-	Layers:
	-	`sha256:3a627337a16f1fe816d85e937dc1f7b5197f38cb5cca6f2c0cf55844ce4291be`  
		Last Modified: Tue, 20 May 2025 01:19:57 GMT  
		Size: 2.5 MB (2487127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d489423aafd3975e52a6534d4f832028ab763822b357af2ceb8365acc1e12fd`  
		Last Modified: Tue, 20 May 2025 01:19:57 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:59a4f3030b626b259b6231a4b9b6897f403bf3ef689a40325e426aa3e32ef0ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44539542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca8f11412f6002775116eb099386c185bd7e87153a9663b088d759eae35ae75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:22:43 GMT
ARG RELEASE
# Wed, 14 May 2025 04:22:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:22:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:22:43 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:22:47 GMT
ADD file:274eb639cc5f95b94465765a3ad611fc9b35404afc1a717ccab5915606fe7258 in / 
# Wed, 14 May 2025 04:22:47 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:96db76e677a2602f064ab776dd6dc077e110206b8dd8f8a61926345fbf423125`  
		Last Modified: Fri, 16 May 2025 13:56:44 GMT  
		Size: 26.8 MB (26769977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ad667c53035533c1f55f593b7cc1dbb724865f97cf066d13c3cad120c739c`  
		Last Modified: Mon, 19 May 2025 23:45:05 GMT  
		Size: 17.8 MB (17769565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3984ee0aefd9f8b84b0a738598daf04d8fe8a9350e22369115288db0cffd1e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b7eb91f49034057720cfe50cf6e2fd3f72c916dddf4f6d2ebd21585c8eacbf`

```dockerfile
```

-	Layers:
	-	`sha256:e16a24b8fe3bf6c0b89952179d4d8cc71070b518ca4e892ac97de2a17f674f7e`  
		Last Modified: Tue, 20 May 2025 01:20:00 GMT  
		Size: 2.5 MB (2488626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bec3889dc4afed5d6e1048e7cce8a27c17dc43f190b47a79a09cd881ce760c`  
		Last Modified: Tue, 20 May 2025 01:20:00 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:50589a9aabd988cc869ffbc5704ba78a17c82ece43a354218e15a88f39b70496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f17ce7fcbff2ca25e1b994a591d496b2d26d41057b72baf1985d193681e897`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:22:25 GMT
ARG RELEASE
# Wed, 14 May 2025 04:22:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:22:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:22:25 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:22:28 GMT
ADD file:fd21715897ee52f2140290b1f7e14ee6da8c539a73b857c5fb652a047dabb640 in / 
# Wed, 14 May 2025 04:22:28 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ec022b1a79b332d6a04d4b3f21fc0806634a7ed2ad52cda89f49f10584782937`  
		Last Modified: Fri, 16 May 2025 13:12:01 GMT  
		Size: 28.3 MB (28282258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d04fa09be15353aaac96582c2c87af01ff778cd01946eec45a230b304ae9a9`  
		Last Modified: Mon, 19 May 2025 23:38:34 GMT  
		Size: 19.1 MB (19063089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5f3b67c30c0b5ea421bfe347333226108d3e76d5b847b8681b62b908d61f2bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8479a686ada3105166445bdf676a0fb1492e2b9c19f65ea2914306b2824cdd6`

```dockerfile
```

-	Layers:
	-	`sha256:012da8aa0d20d0c0d2b0f3d0db8eb1f19a5071893403e3b4ab7e4e3e3f32e893`  
		Last Modified: Tue, 20 May 2025 01:20:03 GMT  
		Size: 2.5 MB (2487384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6716a99bc0e3cb43aed97105ea6b3979c468c2c0f5d562c05c9fa743de9d868a`  
		Last Modified: Tue, 20 May 2025 01:20:04 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b7492924f1a12a8e62069b57c7ae4af2d6f455f4b984bdba8ffa7c2c391c55bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54450516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57175de764491766e2e289b38d80347c222e14ca09d05a0a7070379e922f64bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:22:26 GMT
ARG RELEASE
# Wed, 14 May 2025 04:22:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:22:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:22:27 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:22:30 GMT
ADD file:d9f9e02d15868fd689bdea92a54a568a4592ed5f72cecab767af6481b0a1084f in / 
# Wed, 14 May 2025 04:22:30 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f4262ef187b79c0ab727effac47ef9ee3746639697a95792cb4e866a2dc7b223`  
		Last Modified: Fri, 16 May 2025 13:56:48 GMT  
		Size: 33.0 MB (32973841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02f2f1f81fd8e85949fe8d3c42f2ae5ba4cd7791149a420fe0bbc304b0f3929`  
		Last Modified: Mon, 19 May 2025 23:37:46 GMT  
		Size: 21.5 MB (21476675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1270e012a5a0b67f7302f7b6f0610df5d4e1f4dd2435f9be40e3e492d7950b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2497955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46aa6958da328a4ed10cd0f090d0f339a5288df6c5ed4b52f988bc7edcaf8eb`

```dockerfile
```

-	Layers:
	-	`sha256:45ce9b29fbef12d641a8b1ce4f3fc977e69619307aa6147d0d6a4e7c53f4658d`  
		Last Modified: Tue, 20 May 2025 01:20:07 GMT  
		Size: 2.5 MB (2490945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c52b8677596cf7e455ac8874a4c58768dde50273d03d90eb1ef7b166839bf08`  
		Last Modified: Tue, 20 May 2025 01:20:07 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0de2228abf532efe1250a3c9169f170fb3c9a2992d59fe90579b121c438f09f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49549548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be14bfffaa70c069e68e263c4dd73db6c20a55aa71c6a2fac06fd0cf8f95639`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:51:05 GMT
ARG RELEASE
# Wed, 14 May 2025 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:51:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:51:06 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:51:36 GMT
ADD file:0cd658103d02bf6846dbd2f13752c91538b4521bf27ad3ef8f782d20b0f83446 in / 
# Wed, 14 May 2025 04:51:39 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6b6ac20521bb58fca960ddf3a7c726f8140f436dafe253d6ed5b0749b388fa99`  
		Last Modified: Fri, 16 May 2025 13:56:49 GMT  
		Size: 29.8 MB (29759113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca9b80989299965c9f6755f5840f8c611f6382b2f6f805aec3b88374f28e6de`  
		Last Modified: Tue, 20 May 2025 00:47:54 GMT  
		Size: 19.8 MB (19790435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0417091f147eb81d03e6141745fb444e46ce7c77e3651b54dcd487c2116a9da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca0c46e25437505013e606bed870ac6a7918a57a6a8907f94c8ec3998ee14d6`

```dockerfile
```

-	Layers:
	-	`sha256:63287419aa5ecb28152f543bdfc243d75f76cb26fa2b118f547ce04bfadbc766`  
		Last Modified: Tue, 20 May 2025 01:20:10 GMT  
		Size: 2.5 MB (2480235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a29873d9490bda817a7771b27fe36d87612003503ba2dbba5f1935797f05ef`  
		Last Modified: Tue, 20 May 2025 01:20:10 GMT  
		Size: 7.0 KB (7009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:905e7f87bf29768fb8543fcc7f8e9e99d482930046446ebbd5f534fc5e3ad8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50026657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802de85cee31a011542b55ec0c60df9ba29ebb3e893c68820fb91b6e7fbdff2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:21:47 GMT
ARG RELEASE
# Wed, 14 May 2025 04:21:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:21:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:21:47 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:21:48 GMT
ADD file:b72dde882e0e50b6ae5f82f19274973d603295192777550d7c77d1932792454c in / 
# Wed, 14 May 2025 04:21:48 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:539d1c74edf6527aa984010b302b75b04d20f8f4d72dabf815b2c1be7da9b7a6`  
		Last Modified: Fri, 16 May 2025 13:56:51 GMT  
		Size: 28.6 MB (28570819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16c281c9509afee6a1a1681f462e9e41dda0f3eb4c5efbfbd4c15995792bdc`  
		Last Modified: Mon, 19 May 2025 23:37:17 GMT  
		Size: 21.5 MB (21455838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a0a873a689720fa661343100db1b8dd05cd50a9ac0cf53f85f1ccc560ae7c39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df049d5f44da05fd3f24b76e11201e24e80d4129c78d9a5d0fc0050489ff18e2`

```dockerfile
```

-	Layers:
	-	`sha256:cd2affab62251ab173afd4473c822c70342da3a9d0743bfdbb7024754d72d631`  
		Last Modified: Tue, 20 May 2025 01:20:15 GMT  
		Size: 2.5 MB (2489155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e28e1dc831c97b7b67fddea86ca5488ef8507e45ed9aafe9665f51458b24cc`  
		Last Modified: Tue, 20 May 2025 01:20:16 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json
