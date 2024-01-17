## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:3488a18e7cdd9a642c8a57897e83435ecb96334011d446f33c267397245ccc32
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
$ docker pull buildpack-deps@sha256:c35ef4721ff07e97371000cc01c57546cbd0db469e7e2eb68dc1ecdb5b87289f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40390671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3dbf4f3354eae5e63466282214af949b1c061985e490dfa855c389d1c6fc3a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:17:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b1fdfccfb097e3ea8369bc634c0a794c7f5dfa00a944deeff4a97c9496acd7f`  
		Last Modified: Thu, 04 Jan 2024 20:24:32 GMT  
		Size: 25.8 MB (25769091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7239c158ae97251c79c79b045912b146acfff69748a2146ac66091ac11d3a817`  
		Last Modified: Thu, 04 Jan 2024 20:24:29 GMT  
		Size: 14.6 MB (14621580 bytes)  
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
$ docker pull buildpack-deps@sha256:6821928908b5494c7eefa6dbc125e23bb3c1659bc2e522082425a0e4d1ab9ed9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44784004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedae039e7b5557273a8c4cb57e9ff66352e584f7baa2d11b4d0ebc7a138eb7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0eb0ee1ee32a505c711b23ae33e7ecc888899622d95c7e982ef82dbb529c5d8`  
		Last Modified: Thu, 04 Jan 2024 20:50:14 GMT  
		Size: 28.2 MB (28174524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02199b1c3761965bf141c9010678515a9c50e39cc89d2a830d1dd5d17aa25bc2`  
		Last Modified: Thu, 04 Jan 2024 20:50:13 GMT  
		Size: 16.6 MB (16609480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
