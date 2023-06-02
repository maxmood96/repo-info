## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:dc47bb1c4c1b256c0e150d754e55b480ba6e3244e13b41d352f9b33c5eca2214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d17358e07698d37cf40a859c4ab17466e3f9c482f0fb860d98f04bd8f07cc925
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41377120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b1fde3c2a2a662458127c1dca1876f543e6fc046c10485e1526c51fdcab0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 12:44:41 GMT
ARG RELEASE
# Tue, 09 May 2023 12:44:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 12:44:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 12:44:42 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 12:44:44 GMT
ADD file:f074265119093d25dbd3022b9335bcff83e7bd893a43de3f4c62e7b9f86f3180 in / 
# Tue, 09 May 2023 12:44:44 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f0f0a5354c0ae208576c462d933b6dd9937ba3a0e0109fe6aaf52332686d5c4c`  
		Last Modified: Wed, 17 May 2023 00:43:35 GMT  
		Size: 27.6 MB (27616500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3f8ccb1549a815e890ec3e685f1dc0553f12021c3f3a0c180f4b7205baeca4`  
		Last Modified: Wed, 17 May 2023 00:43:33 GMT  
		Size: 13.8 MB (13760620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:86361bf7b767f1f236dcbba6e905edddd42881fcbf88cf7d923427d68494034c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38035079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeec579c9e68ef638a9bade1608a0ef512e0bc00a6621cfc9cfecb5a72a4be54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:22 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:25 GMT
ADD file:c7522b8ff46586b3057c8eae94d6cfc77299a4f2ccc3762e6263780ccc7c82c0 in / 
# Sat, 20 May 2023 16:58:25 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:51:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:562137b754651e3134bc25cd5345aa8ee488e4018a6b98dca99da8c6a698516c`  
		Last Modified: Thu, 01 Jun 2023 23:57:12 GMT  
		Size: 25.4 MB (25360044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e14e8697677cc5b120d6102abcd07fc40bbe1f33ce15bf65b69c87877e6721`  
		Last Modified: Thu, 01 Jun 2023 23:57:10 GMT  
		Size: 12.7 MB (12675035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2415e559257d07fc2ee42bf19945272be52768b831037d9e239d731801fcc7bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40390908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6cdab424fa1ba50b31bce8ca98ef10f7311eb46f3564b25da9c7e93327122e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:34 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:36 GMT
ADD file:39dff3364ce4bb79539ed5e58493be16a66d424e605cb774559830ba8452bc4d in / 
# Sat, 20 May 2023 16:59:37 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:01:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e1b7a20de65cc40ff963f40b4d97f1bea4a466e8941c9538a13270a948c2a7`  
		Last Modified: Fri, 02 Jun 2023 00:06:42 GMT  
		Size: 27.0 MB (27042242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2739609605be7ce435def151c1c15562a7fbd66a303de8403e883c503df71c5c`  
		Last Modified: Fri, 02 Jun 2023 00:06:40 GMT  
		Size: 13.3 MB (13348666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:73101c06c050386fa14905c99938156d533fdeb920f959067b4003151ae0ebd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47862621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefd459e0dc408e4ff00877aeef78d84a3827e2a99dd001cd8d5ee911941f5cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 12:44:00 GMT
ARG RELEASE
# Tue, 09 May 2023 12:44:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 12:44:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 12:44:00 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 12:44:03 GMT
ADD file:d42dac32e11311d9b5e412834823455c0173f98c6a52bbb537a30dffb3bc872f in / 
# Tue, 09 May 2023 12:44:03 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fa2defe9dba792ccace369ff4376838b0ce6d5a66b5f5203aa26761e8d1494e0`  
		Last Modified: Wed, 17 May 2023 00:54:29 GMT  
		Size: 32.0 MB (32008882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ccf43574a204fb203da7c5786f2d89752ab4c468f685736027513b4113c7cf`  
		Last Modified: Wed, 17 May 2023 00:54:22 GMT  
		Size: 15.9 MB (15853739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:24bf651c84d530511ed22d8237e59b75b56eb0cea62e6b1d1e56f4b3ef53f2d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40250485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c887c2df5762cd40c07a3205a8efd617ba920b602f166cdaa63ca53414c043c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:20 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:22 GMT
ADD file:fb602b3f6c251d8267de1cf0525d0b38aab5966c848182d037bb2890557f0a6e in / 
# Sat, 20 May 2023 16:59:22 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6197ead7faf6fa2f836b159dd66c603a28c581c4e273f6b664c86588a78ec95`  
		Last Modified: Thu, 01 Jun 2023 23:20:39 GMT  
		Size: 26.2 MB (26231487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98abbd746ec759f3d8e8b447407b1e0248bc8e38e037360bdcebb69899e8cd07`  
		Last Modified: Thu, 01 Jun 2023 23:20:38 GMT  
		Size: 14.0 MB (14018998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
