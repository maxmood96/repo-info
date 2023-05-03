## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:5da51c9251ae8075af3deb7452d6d858aedd550f55714af037046c669c9d6847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:ce7f6664be1081be78dfcf319cb11d7bceeef17b32df373282a66fe940e47f6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0120ea4307c597784895e9f539a67d88239d2c71ebfa830195fa2a650e4f3b5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cc1fe050fbd8eee8b0e2ef684c783d2c269fb7f61a0df0dee4639340bf612925`  
		Last Modified: Thu, 20 Apr 2023 18:59:08 GMT  
		Size: 26.8 MB (26825231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2d379e00f7bf822cf2133d5f353ef6a5e4621a2c34334f99d800bb6440b0e97a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24632909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdc4400067184574d122f092a66f0f8d2ed3d785bb9cbd8be35a0093b594151`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:604aa9b61f196d7ae0abd17a6d697aeab5a916fb6500d6887e59a05d362a1a06`  
		Last Modified: Thu, 20 Apr 2023 18:59:21 GMT  
		Size: 24.6 MB (24632909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e73844b55fb1ba94e595d64538acfcc1c4840b750f967ce368d91a51fa5007ee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513df0534cf35764514504f883f2163eb1bda7be89a511cad89c8c7d38b2626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0da974cf49e20cf8a8d93e9fda8598c48fbe9736275600c0efafa363ab592eb2`  
		Last Modified: Thu, 20 Apr 2023 18:59:15 GMT  
		Size: 26.1 MB (26079115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f871f7609ee2d4dcf0ab6d2597e9c3e425482e189c7abff04de33ff54511759b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb6dcc0aed4be2d1b12ad54505515a29a6eef8502a249ea14dfb671f3ad9d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea416d41ef40856710483d8bb41ae5d7cc41d5da1075df7ef64e9694b18b3e0f`  
		Last Modified: Sat, 15 Apr 2023 05:21:01 GMT  
		Size: 31.0 MB (31018597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:3af6f4dd8a997017ff74949f2f4e88d672dfa28b5ea06e4093a3e15193bb9391
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25705932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa77ff3a8aeaf751ae3c673bb074b5f67528671ede73189cecded4d61348f7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6dd1be43160c095f202288009f4efedacf98863e9604b1af368e386488389a6`  
		Last Modified: Sat, 15 Apr 2023 05:21:07 GMT  
		Size: 25.7 MB (25705932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
