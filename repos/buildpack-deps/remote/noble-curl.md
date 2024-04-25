## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:fb2a1756b2d61c1ecb16a29b654e6758185ee358094cbd969bbde6407d6e1baa
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
$ docker pull buildpack-deps@sha256:e8e1b17172525934b624735cf1825a1bfef021be6b4565165b99e2540ff25df9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44002313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72bc4a91a07687b483c63fe011d45247aa59acefc1db19f8f881b1ddf5e3938`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:34:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f5159575f7bbbce11277d1532c12d73076587ebb492562917370449a8c5e7fa`  
		Last Modified: Wed, 24 Apr 2024 17:16:59 GMT  
		Size: 29.7 MB (29702068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdccdd8b38d211dca25619ea8b5b92600ec3e2caa4ff8d1b944fe31205f9fc9`  
		Last Modified: Thu, 25 Apr 2024 21:45:37 GMT  
		Size: 14.3 MB (14300245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:805692683176020a8aec14bfc98c53183791de85cb8d604a7431b32ab7d41d1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40276253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56f35c12b0c1f7325582061de4ad5c839511bbb28e0d100dc607f0678878114`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:39 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:42 GMT
ADD file:158f9c2033bf15aea7323a8fc02ed64bb41784f98f36b5faf68a959346a86757 in / 
# Tue, 23 Apr 2024 22:03:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e440e8b3da7c90c5ade14456a5cbffec3e72a2bb2eb7d20b5c4eb2e63407ceee`  
		Last Modified: Thu, 25 Apr 2024 21:22:19 GMT  
		Size: 27.0 MB (26953117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b7edd08b76e28f02abdd681d6fa83e384b4a379d227cfacecec42f61a1dbf4`  
		Last Modified: Thu, 25 Apr 2024 21:22:17 GMT  
		Size: 13.3 MB (13323136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:578930af980d0fc39a750c94040fd07f21b38a03e616048eaed2c41c8c9159e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43170189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cab8b7c3013357e962dd445d748c46322e4ed22c6cd7f76891773ce669c82f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:43 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:45 GMT
ADD file:61020b87bc980abd05e75207205df7ecca6ea7023b3a5e804aabded0eebbf2e7 in / 
# Tue, 23 Apr 2024 22:03:45 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec7cb58592b61e9a11cec56cc368247d061905f8eee62423f6dddd42173504b2`  
		Last Modified: Wed, 24 Apr 2024 17:24:38 GMT  
		Size: 29.0 MB (29037830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bb3095dea3c00ae7a36d74265d34ddcbe154310bbaf23a8c2f113439f7b67b`  
		Last Modified: Thu, 25 Apr 2024 21:47:36 GMT  
		Size: 14.1 MB (14132359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2eb8aad0a216b938c14f27b9c38fb54d04b5348fd3c5ac6d15f064a9c18daf2c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51441884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95bb4101c15e50b8a5ffe6fb04e2f7990c400204d68c647d24c519002c2d0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:16:12 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:16:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:16:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:16:16 GMT
ADD file:7fd16485139d3989a1a5565c0d7fb14bb79403891eb470189d51dac672fd641b in / 
# Tue, 23 Apr 2024 22:16:16 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:52:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:376893c0d3e66eb0681db32a86ec72e75bfe0975d26041f1523ff33804bfdee9`  
		Last Modified: Thu, 25 Apr 2024 22:07:47 GMT  
		Size: 34.6 MB (34574708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2023c2abeac79352985ebf619d415cc8fa67dddc498f6ad865dbc3d20a758b`  
		Last Modified: Thu, 25 Apr 2024 22:07:43 GMT  
		Size: 16.9 MB (16867176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fc831779fb6c27980929aa714f8504f0d9aeb5817683169eee2f40fe529c995d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45501157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fc8603d4bea81767f2180730bc8cf2fccc42f29e89928746e2b4523153a8d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:59 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:01:01 GMT
ADD file:a8f6a75bd4e0f37e8479b0e5c1fd1ab287398559996948607323ac5831f29411 in / 
# Tue, 23 Apr 2024 22:01:01 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09891c72d44d843dec0981794f145f31192710104498499b3283205e955a4699`  
		Last Modified: Thu, 25 Apr 2024 21:00:21 GMT  
		Size: 29.8 MB (29781724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2975750ba9fad7e23fa7d0af87613454caf33ef321c9ac49fa93bf1d2bfe84a`  
		Last Modified: Thu, 25 Apr 2024 21:00:19 GMT  
		Size: 15.7 MB (15719433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
