## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:9c0757595f62f371ca25618d6b139f3ce64c39d7b3ea5ac019d3d563faf3f29b
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
$ docker pull buildpack-deps@sha256:a06a7ebce6595efe360b0e3d62542a062f8766fcc3aca19245a59bc94cdee8ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44007034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81652d373be9023a86498dfcf1d33190c332460c7e0609f64b3a1b0518a5017`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea5bac13515fdc1a8104c4b6ea8a3b1a95b23c5aca6d0d4c9678d4dbd51f787`  
		Last Modified: Thu, 02 May 2024 02:14:27 GMT  
		Size: 14.3 MB (14304582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b7f9e574ae10c499bb582afd213d19773c7ea7b994ae78fee9546d97fd0d6a3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40283190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66423aea856bbd835e6c0cf186c7fba9450b18c07a9ddad9d5ba9f8522f75b1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 17:03:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 17:03:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 17:03:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 17:03:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 17:03:38 GMT
ADD file:7b9ebeed2b8df3ae6b4ff0b90cb86423ff21019cca623cd8f5ffaeedebc50bef in / 
# Mon, 29 Apr 2024 17:03:38 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:65b0f107a3b2a3765c847470cc1b37265cdb4ec78f1b5b17b6936546f15e2381`  
		Last Modified: Thu, 02 May 2024 02:12:18 GMT  
		Size: 27.0 MB (26956922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2009af8124e8bc3b99916b5796900bb049316889c95b2415fd0546099a15fbac`  
		Last Modified: Thu, 02 May 2024 02:12:17 GMT  
		Size: 13.3 MB (13326268 bytes)  
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
$ docker pull buildpack-deps@sha256:5c8f99250df0a38f3742b5755be9b7a72ae85e35ca9a4bcf5857f942c2f99d53
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51450130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4661ceee5e4705411b3f2d661821784d7a5a38b637d29af9b6fe3e29b5e1c890`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:36:39 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:36:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:36:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:36:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:36:42 GMT
ADD file:c915ac180ad59faba89e9e3f73473adedd3ac5b7024bea2fe61b266b3efc1267 in / 
# Mon, 29 Apr 2024 16:36:42 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bcb8c42b2752babcd7ef1c98e380f22f0fe7f25521a416951d4cd54bb4cb300`  
		Last Modified: Thu, 02 May 2024 02:33:48 GMT  
		Size: 34.6 MB (34579045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311118f71d2a44d1b56b9473b56c32fdfc1087ec55036a3248875324836f0765`  
		Last Modified: Thu, 02 May 2024 02:33:40 GMT  
		Size: 16.9 MB (16871085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b7ee9ac006e0ed5ff54a4d0fbc7cf631bfa545ff7c97917ac1c2179864e2e80d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45504768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64df918ebbc0d2481fb8cbaab93def7982402437f455461092fb1978d47815ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:68e0be12c8304c831d669224097b6db6b2c5123796652f8911f2245c0f955227`  
		Last Modified: Thu, 02 May 2024 01:35:40 GMT  
		Size: 29.8 MB (29782463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a326658ec81d60132e0e611daac8eae9a8b5a44e3daf1e55494e0fd34099b201`  
		Last Modified: Thu, 02 May 2024 01:35:38 GMT  
		Size: 15.7 MB (15722305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
