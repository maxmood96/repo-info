## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:720cff65ba9a2dd6357338a52ab781665b3c4039fe48a70af1d404bb78e1cceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:002da05f9df97b31ef836b483a61ed01d3331ed704492ee4af14d639e70063bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76493398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94047d7f8b431825db72b9fb121c25b457aa8636d32cbe8294d878a5142ab1db`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:04 GMT
ADD file:ef50fe9796d01aa6d5f96fd48a91fa7572137f06bc61426966088466af436be1 in / 
# Sat, 30 Mar 2024 20:53:04 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:01a297f066f8fc0bbbe233ce2512fb4efd2ccfdec3a317e7b2f796cfcc8a6851`  
		Last Modified: Sat, 30 Mar 2024 20:55:42 GMT  
		Size: 52.3 MB (52332501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa6c10db0a79c5f80b9d9dd9d4c7f1aac92357e9f7e2d86820642467e3599d`  
		Last Modified: Sat, 30 Mar 2024 21:43:48 GMT  
		Size: 24.2 MB (24160897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7fbfa81d59aac0db3ce9fc149b2457cbad7de0c2a4b87c62b9a1322efc1316a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72463645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d657f7569f9296996cb49331191c85a53b0ff696831458f2abd425216f4ee64c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:14 GMT
ADD file:610edad9ac2672f29e192282a6bfb0a5bc5909a7410ce328dcee965f697f3e7c in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e2d9fb5eade7bdb964f6a5e67b4501451648660fd642b9b8493a947178b448bc`  
		Last Modified: Sat, 30 Mar 2024 20:54:36 GMT  
		Size: 49.4 MB (49422214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a8b4d238b7be08d593a4029f99f33372bcab2e8fdc18f8284effa4d1c0d04`  
		Last Modified: Sat, 30 Mar 2024 21:20:53 GMT  
		Size: 23.0 MB (23041431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e2e75a10eb04172119c721e9cfdb6c6dd68fcccaa2f72a7500e10ece8d5ef33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69275575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22849dd906c5988b8dbecb1128db23dcdb6bc204c546d5dfcc9c7f202c36720b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:316e1fa8a278128ad74632d6c2644dea76ab06f0478bbb6bc10e2b7da5bffee0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76072170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490610d0fdef66fd582ebd89efbdbfa1f998860955e5be3e5ea5ac9237ae53b1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:34 GMT
ADD file:4e62b2db165216904b425ba83d0b0d4c6186d832ff996f8b8c3b063774e053c6 in / 
# Sat, 30 Mar 2024 20:55:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:07df543a1d7c9498d71f3bbefc8b63ef01e65874f69ca50b6719f8aa26631ba2`  
		Last Modified: Sat, 30 Mar 2024 20:58:03 GMT  
		Size: 52.2 MB (52193164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8de779e2187666ead1e28d72960c6006d9591b628ff3bcf5f05debb1f209af`  
		Last Modified: Sat, 30 Mar 2024 21:43:47 GMT  
		Size: 23.9 MB (23879006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ade99aca5a25a9ccd47b950d25bce57189ae06309fec207a419bd20d9204481e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78464402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7140bd1b11c3401b355ccc13586f05f2d2fb3e2ec6fbf6f177c608da01b21968`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:363c0c44809b184ca8136ce186fb7b835d52282b57b2a32140cf8abaadb7c521
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76035641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2592a789f614b82ffe8267610de4d3d39c0e9172725f22ab8e5a3624e774be9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9ef7db1d4a6348f18c0d9380d0ca7dfd813434858666fc4eb03ff5eceeb9042b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82505891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6eb67d19e8d3ea6600b0e12284439dcb5958712689cf4f73250cd97c1a2b5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:83f705be493e94d0f9dc88d3ee5b6ed40435cb2c2fc2d3f80bf6fab9ee228443
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77035318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1b4ae5479896b2c5ee8df61f53aa58a57a6f09cff15b2c8a20903b75650393`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:17 GMT
ADD file:a763a87b7a749afb8ffcbc72555a671734dd9d842834384eebb8dd784135bfc9 in / 
# Tue, 12 Mar 2024 01:12:19 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:26:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2f13ce6fc956957d2abf0abd272bd88a159c9cdf4a731647c572eb2581973c57`  
		Last Modified: Tue, 12 Mar 2024 01:23:47 GMT  
		Size: 51.7 MB (51738519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4953941dae1a90e29387e6e32120bb7c2ebca24adab5d68977c75cbd85a709bf`  
		Last Modified: Tue, 12 Mar 2024 02:50:10 GMT  
		Size: 25.3 MB (25296799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
