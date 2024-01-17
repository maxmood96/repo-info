## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:0db1a57b4cd2bc75702257eb741633a718b356e5d632ccb49081db8f0a9e6c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e871ce4fefe194ad023e3d00d740681e93aea65068d6e9e2ca35409605ee16ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44038436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9521c467ffb4e332766da6de9453b76f101586bd9c0becdb05ddd1be0114b5a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 08:48:30 GMT
ARG RELEASE
# Mon, 15 Jan 2024 08:48:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 08:48:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 08:48:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 08:48:31 GMT
ADD file:e5e7262b8cac5f725d4433779ecfbcadb4025759c5973a276b344033d087bfb3 in / 
# Mon, 15 Jan 2024 08:48:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc35f4f5ecaa073076bdb6773257cebc5c5f2ad32bf5f3c21b5f0f462cc825ab`  
		Last Modified: Wed, 17 Jan 2024 07:40:47 GMT  
		Size: 30.3 MB (30313466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fc63ab3c7470561d0ea5fde5977e2154db737dcd470c977cd0202fbe1cb86d`  
		Last Modified: Wed, 17 Jan 2024 08:04:45 GMT  
		Size: 13.7 MB (13724970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f2401f652a20b2623c44001cde591218eabc3d5452995fcee057117861774e29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40366073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639be7a48b72ddfec819f23fc543ebfa22218437190793a7ba71b10cdc857ad8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 08:56:13 GMT
ARG RELEASE
# Mon, 15 Jan 2024 08:56:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 08:56:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 08:56:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 08:56:15 GMT
ADD file:6e0878d28c3fc86e0e1bb0a7bf6887d1a811d12a78af18b686239c441c9285a5 in / 
# Mon, 15 Jan 2024 08:56:16 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 09:30:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d881640c2046402bb8bd31e62927bb5177c9abededab0756118ec8b20f33fd7b`  
		Last Modified: Wed, 17 Jan 2024 09:37:42 GMT  
		Size: 25.7 MB (25746745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188c4ee23b8759f85eafbe834c18a64e24977df1a29766749ac5a14f3c11fbdc`  
		Last Modified: Wed, 17 Jan 2024 09:37:39 GMT  
		Size: 14.6 MB (14619328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5c83f57c85723d1097b99da03a6fe892856918e52b14d7c08278fcb18128b0a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42918245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dada348cce8da2750c1487898a54fa6bd1bda97d8b935aa03bfb312942c1060d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 09:01:27 GMT
ARG RELEASE
# Mon, 15 Jan 2024 09:01:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 09:01:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 09:01:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 09:01:37 GMT
ADD file:50cd35ee54b9e6bef21c07d3de865616eca5989c84802fb5387d3e67116b92ef in / 
# Mon, 15 Jan 2024 09:01:38 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:520813436ddf1775384a8b61d3beb75fb5c87ba7ba0ce3f9840941e56bb9e5a3`  
		Last Modified: Wed, 17 Jan 2024 07:27:29 GMT  
		Size: 27.4 MB (27403386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc92cb739627d08f68672a7bc2d006b5cee710ee782a771e88fe36a8eed57f28`  
		Last Modified: Wed, 17 Jan 2024 07:27:27 GMT  
		Size: 15.5 MB (15514859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9c7cc1159ee36a8dda4c554d2a10473fdd653e583d3c23f932b5dd176cc96e01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50942483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229a6ba5ab1d5fcef4755335b821fdc1c7f91eb5785e243282ed83b8ad0c7dc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 08:51:02 GMT
ARG RELEASE
# Mon, 15 Jan 2024 08:51:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 08:51:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 08:51:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 08:51:05 GMT
ADD file:5fe12e290a829b7d5ff1eef600b9e7e81a107059fdfd6c8195467a8e2f0a0463 in / 
# Mon, 15 Jan 2024 08:51:05 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:49:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5d48a6050ca99416832e234804b8b3fb2aecfab55da73b3f44bf60caf56ec7`  
		Last Modified: Wed, 17 Jan 2024 07:58:48 GMT  
		Size: 32.4 MB (32381280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6cd7f36bfac4a5a101ecc849afd614052d279b532e79535e7042b63ca4cdef`  
		Last Modified: Wed, 17 Jan 2024 07:59:11 GMT  
		Size: 18.6 MB (18561203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:364b16c374185728d13dc40c576733623256f7b9a1b546c80423acbabf849169
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44797579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebdd192aeab88234de9d8e88468fc2efc1f103884197bbdd04da416a1fb6be6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 09:22:57 GMT
ARG RELEASE
# Mon, 15 Jan 2024 09:22:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 09:22:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 09:22:57 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 09:22:59 GMT
ADD file:11ddb4e9fcd108f4fd5ed6275baea08549f82457f582ce2774730207b53cef37 in / 
# Mon, 15 Jan 2024 09:22:59 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:354de95796a22c0af472e80696592950b557d1919b437dc9440875ccdcb3e54a`  
		Last Modified: Wed, 17 Jan 2024 10:39:39 GMT  
		Size: 28.2 MB (28172867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b188be263045b808aaece198ec70f2bab1f360333a2b203f57d8f89050abe5`  
		Last Modified: Wed, 17 Jan 2024 10:39:38 GMT  
		Size: 16.6 MB (16624712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
