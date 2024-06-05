<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:24.10`](#ubuntu2410)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240530`](#ubuntufocal-20240530)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240530`](#ubuntujammy-20240530)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20240530`](#ubuntumantic-20240530)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240530`](#ubuntunoble-20240530)
-	[`ubuntu:oracular`](#ubuntuoracular)
-	[`ubuntu:oracular-20240527`](#ubuntuoracular-20240527)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:e4c02475c7c9c43f8f5bf595d5260a84e1b44e49d9c5ece6d3e5dc6a0a5835a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:d86db849e59626d94f768c679aba441163c996caf7a3426f44924d0239ffe03f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5250218d28ad6612bf653eced407165dd6475a4daf9210b299fed991e172e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c90819a01d32d552ec8faf5bffc7ea2f3c9cf130ba5ce78804a07aa75a36751a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b69318504f466a22672e9fc0fcb8f4afb9d8701f88dda485c6a786bf8e3c21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:50 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:50 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:43:02 GMT
ADD file:5789980ed37544805bfc38f68255149cf4ceac7689ffcbcf606720b1b7170733 in / 
# Sat, 27 Apr 2024 14:43:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1012ed6a5d444a056b71f02e12cc46eb753d7e45477e106ebd9f6e94188a82f5`  
		Last Modified: Sat, 27 Apr 2024 14:55:09 GMT  
		Size: 23.6 MB (23623650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6edb9576e2a2080a42e4e0e9a6bc0bd91a2bf06375f9832d400bf33841d35ece
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583f1722e16e377baf906fee1ec6a9fda85ff7f3d13f536f912998601fd85ed8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ab24b025f37cc43b5958527e6fce64b2d1e36c4123010887f906d817956ae4cf
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32077140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660a3306db77bc0d9fd3510f59ecfdc664e5868e872bc91faf71f5796434f198`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:bec8a96229e24d6a9b3c333071b645c7aa7d864596ac609fbbbc89d990312394
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9374e168016e3656c0194d188dfb164fb07c23e9386799c0aec38196d359c357`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:39ab14240b6da1cb8c34bd4f498b90b7cf3b6c6aa2d524f45c9501038d6b2709
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:94db6b944510db19c0ff5eb13281cf166abfe6f9e01a6f8e716e976664537c60
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c845845b7de8024a1ad9f6e7fd08964502a0b423aa8de631ef521863873884`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2f63021dc56651000aa1e250d42c3aa898a5cd61120aeb8daf9e7e0fd20b84e5
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26639789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0514f6822f381d7a240dfe8c419582164af5ad9465c1a95b69d1b44daedabdb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:35:06 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:35:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:35:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:35:06 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:35:17 GMT
ADD file:ab2e95a123b006ac900aaaf0d1858b88941c8d319f47e41733db6f0f5fe98b87 in / 
# Sat, 27 Apr 2024 14:35:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5b4213824fc3515b68e6844d3fc289ae00ef8cd07ddcd43856c3ad7faea16d4`  
		Last Modified: Sat, 27 Apr 2024 14:45:43 GMT  
		Size: 26.6 MB (26639789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ee2717369ac272fb83a9035762820588e77747d01a7e2fa1f36ded5a7fe672e4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27361782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442ff3b14f13ebbe3ea796b0963204140e94f9e9fc0776217cfb5a2d723fdd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8d6c06273eed7afd8e0f61334979062d373ffc7dfeb6e4a78ad8a78e688d9646
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34460693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1667f256c50ba367c051f8b8fc415211939bf5bd64beef7e4328e0fd068a5f8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:f743197c351e3d513890e8ac18fca1120555b211d848a15ecfb293cca5b31787
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95834ae443acf6a0548627723a599f867656b8f50a108c0f6375717f0c81294e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:04f8e2f61d65d5f65cae9f9f88dda1c4bf72abd45de33cfb1ceda768b537ce6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:c57e8a329cd805f341ed7ee7fcc010761b29b9b8771b02a4f74fc794f1d7eac5
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27234148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77081d4f1e7217ffd2b55df73979d33fd493ad941b3c1f67f1e2364b9ee7672f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cd0bff360addc3363f9442a3e0b72ff44a74ccc0120d0fc49dfe793035242642`  
		Last Modified: Thu, 30 May 2024 04:52:39 GMT  
		Size: 27.2 MB (27234148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:76e4b6173670f4ecc21ea3264690d8c7bafd9863bd7cd2ce0f1bc4987f61bdab
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24888998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fe1df8338a7972be9f896df29e704342b3ebb3e8396f4d57844f40d2997a60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:05:53 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:05:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:05:59 GMT
ADD file:36a9fb96170feb2e8bb6dfda0793b5f7069593502c61024a6ed3d84eb01afdaf in / 
# Mon, 29 Apr 2024 16:05:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0fe43babe382dda04daea3eee6f3cad8ebf71da7df35af926aeaa07b253b2d8`  
		Last Modified: Mon, 29 Apr 2024 16:18:55 GMT  
		Size: 24.9 MB (24888998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:72c9c923b9807a752ba9c8ba41432e62bb88312de9d15b536caeaf3ea5965ad5
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26418209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ba2bc085030d6d70a7361cd2dcbfa62d90628bda1bbc5081ef895027b5f2f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9610c9b6cbed27d1798b34c30c1a9db4755a2ede67a8f5a4e9ad8821ac6afc22`  
		Last Modified: Thu, 30 May 2024 04:52:46 GMT  
		Size: 26.4 MB (26418209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:487346421a0fbd5887b0d4570b6543067670232c69d369a60626f8198a35d288
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31368685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c3391bd71baa0a068fcc1e9c12429aceeb5223ab8dee7bcc4fb7d15f57bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ec16e64158cc3af55ad7c1876c57891971c632dd2c1a37e5ffc42e9f412e13c`  
		Last Modified: Thu, 30 May 2024 04:52:59 GMT  
		Size: 31.4 MB (31368685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:d07675e241e1534e8947a5ba1895cee47b8a61643d71ec14c1e1ea8708cc47ea
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c9e0438dbf2d840e64f8c8f1ad100d0e8b7278efbd623aa303367d7e6022d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c3890b7f26f4184d913e16fb22de153b50817b714156ed910d8cc21a32a2a2df`  
		Last Modified: Thu, 30 May 2024 04:53:06 GMT  
		Size: 27.3 MB (27332665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:f7e60f6ed8e4233637730cf2fbcf17bd1d8855d3d25b0462637bb94efa839860
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:24.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:c279a739b31ead4ebc3e9ce04937eb8b612799b52c26133eb3b4a056d08c31a6
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28872332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c0145030df106e60e5d99149d69810db23b869ff0d3c9d236279a5a7bbb6b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00d679a470c495ef7d52e70bcd7a008f4983530b67653e63e9d3cd27fade63d7`  
		Last Modified: Thu, 30 May 2024 06:26:08 GMT  
		Size: 28.9 MB (28872332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d69717588093ca3aaa2b5721ba1b349c665417ed60509877a15538da12b73773
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26112818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f089e57ee3b8d40972824b4baff3317e5c80dcb31e0b3e79751890479a9f49`
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
```

-	Layers:
	-	`sha256:99c7292dd1d06c9e121ff292a5057d7ae7d531a72e4201db6db2e26338b60466`  
		Last Modified: Mon, 29 Apr 2024 17:08:56 GMT  
		Size: 26.1 MB (26112818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:17c24d16d63d2d089db74c2ed3e99c1ab0fd3f4f93c00b04afa8793fa793626c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28018664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc33afd4c9a541270cdae3de1f78190908ffb34081e40e636fb7fec32434e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa21f24e1940b1a682fe8effed3c9dcce0642450f7b085da08ebf725f3b70f1c`  
		Last Modified: Thu, 30 May 2024 06:26:14 GMT  
		Size: 28.0 MB (28018664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ae33d4f9381714cc1c716ccef9752aca7fcd52b5485620e8507eccd3f1a35b54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33492344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4057f9f3b277758117225481bde62f58a2690edc984fe799daa1ae9b44f11f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:059424863d1c38263ac74ee9c9b4b5d5df9febb81b7b0cd7ad14f5b351708678`  
		Last Modified: Thu, 30 May 2024 06:26:26 GMT  
		Size: 33.5 MB (33492344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:4f6b0e5e7212399168bd61c7b156c803d884b7a6dec07f387ec12cac2f2e5e86
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29167835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba52fbdc7969b516d0a34517f0853f3e95874636b88ec9e2c3d15db33cff1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dfeef248fc5b7b7a6c3c4f71a30ae3f5c8fc461af91cee39c368079dbaa3351a`  
		Last Modified: Thu, 30 May 2024 06:26:32 GMT  
		Size: 29.2 MB (29167835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.10`

```console
$ docker pull ubuntu@sha256:4cfc6f38ba7d6bdbacd66b7877013b54193e8bf89ce9d31742b6a7ff5d3ccb7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:24.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:f0e91d9bc9a7a5bea3bb3a985f790da4c54b8a71459b9a05889b8bca94136dce
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29771141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195922705d1ac968c7a2957347fb5dcfab18beeb51127d9857538cbd1385d23d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:26:46 GMT
ARG RELEASE
# Mon, 27 May 2024 16:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:26:47 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:26:48 GMT
ADD file:7494747de214fc382e1eb68d321438cc6d5867ef746ee5d62919406473341936 in / 
# Mon, 27 May 2024 16:26:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ef7bc4a68771f815262911dbd473dbd9fcd723dcfd13a33b1d0a260a29e9825d`  
		Last Modified: Mon, 27 May 2024 16:40:43 GMT  
		Size: 29.8 MB (29771141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6015d5cffae622f7779768d05d3f86be6663b53f3e71c5f15878c12cdb19dbe0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28888016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39255a8b34c94b48a216a3a04ffb909fdbdcfaa99b33562e7e5a631dea13d6e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:29:14 GMT
ARG RELEASE
# Mon, 27 May 2024 16:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:29:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:29:14 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:29:21 GMT
ADD file:58d1f4adeda18acaf194d00b71d74450c8fbd68230273d1f50b8c0dd22799461 in / 
# Mon, 27 May 2024 16:29:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca17094f6427bbffbfb5aa37095119c9ff0e754728b899b6364837de4f71deef`  
		Last Modified: Mon, 27 May 2024 16:40:49 GMT  
		Size: 28.9 MB (28888016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:4ba709a557c76c77df139e664c1fda668f0298d49513b21fffca19384bf64233
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34498286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2718335dd3099fca397f699ba7511d175af30e6649ea9978052fbb9109b8b345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:23:19 GMT
ARG RELEASE
# Mon, 27 May 2024 16:23:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:23:19 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:23:23 GMT
ADD file:19080182caa6d088e7b16cfb92ba73313501dd5937d3d756cfde855b0419151e in / 
# Mon, 27 May 2024 16:23:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95deb0d73890be47bc15a9488fe4038e8df63561527f7d9715cff885b11314f7`  
		Last Modified: Mon, 27 May 2024 16:41:02 GMT  
		Size: 34.5 MB (34498286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:51e606cd0208737194fbc3ea9cf1e32c90f2e9545bfae7c0f00f353def77f813
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30052199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c182ab0438cec99577a10b037c05f21638172ab72da06857666bb2178fc17c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:31:05 GMT
ARG RELEASE
# Mon, 27 May 2024 16:31:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:31:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:31:05 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:31:08 GMT
ADD file:37d45bf71eb61d46dd7a2368a314709dd743398ebd7e36282eac12ea29af149b in / 
# Mon, 27 May 2024 16:31:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:99b70a6005559ee2ae1c1ab75f5868065283a5a84a8ec4ef3251161922a3df4f`  
		Last Modified: Mon, 27 May 2024 16:41:08 GMT  
		Size: 30.1 MB (30052199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:8ff57fa4112e0a3d1def1702e0274523f97daaec0414554c1e716cc7d3660ed5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:f0e91d9bc9a7a5bea3bb3a985f790da4c54b8a71459b9a05889b8bca94136dce
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29771141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195922705d1ac968c7a2957347fb5dcfab18beeb51127d9857538cbd1385d23d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:26:46 GMT
ARG RELEASE
# Mon, 27 May 2024 16:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:26:47 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:26:48 GMT
ADD file:7494747de214fc382e1eb68d321438cc6d5867ef746ee5d62919406473341936 in / 
# Mon, 27 May 2024 16:26:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ef7bc4a68771f815262911dbd473dbd9fcd723dcfd13a33b1d0a260a29e9825d`  
		Last Modified: Mon, 27 May 2024 16:40:43 GMT  
		Size: 29.8 MB (29771141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b1bac55096baf00b115c63c90d652bc3b61881fa892fcf907d93ac9813b94614
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26102916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab356d34f77ef44955e18cf6d2158771582951f7abef1cf8dbe21f65aa1a8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:55 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:08:04 GMT
ADD file:969299ec7ff65f7cea645f47c5b49e4d321bc39113984c894021da377f00b25a in / 
# Sun, 07 Apr 2024 17:08:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6361534ea0ef9c51acf151b33e52b03a45660ec66315943c40ec2d02634f99bc`  
		Last Modified: Sun, 07 Apr 2024 17:19:17 GMT  
		Size: 26.1 MB (26102916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6015d5cffae622f7779768d05d3f86be6663b53f3e71c5f15878c12cdb19dbe0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28888016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39255a8b34c94b48a216a3a04ffb909fdbdcfaa99b33562e7e5a631dea13d6e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:29:14 GMT
ARG RELEASE
# Mon, 27 May 2024 16:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:29:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:29:14 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:29:21 GMT
ADD file:58d1f4adeda18acaf194d00b71d74450c8fbd68230273d1f50b8c0dd22799461 in / 
# Mon, 27 May 2024 16:29:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca17094f6427bbffbfb5aa37095119c9ff0e754728b899b6364837de4f71deef`  
		Last Modified: Mon, 27 May 2024 16:40:49 GMT  
		Size: 28.9 MB (28888016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:4ba709a557c76c77df139e664c1fda668f0298d49513b21fffca19384bf64233
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34498286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2718335dd3099fca397f699ba7511d175af30e6649ea9978052fbb9109b8b345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:23:19 GMT
ARG RELEASE
# Mon, 27 May 2024 16:23:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:23:19 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:23:23 GMT
ADD file:19080182caa6d088e7b16cfb92ba73313501dd5937d3d756cfde855b0419151e in / 
# Mon, 27 May 2024 16:23:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95deb0d73890be47bc15a9488fe4038e8df63561527f7d9715cff885b11314f7`  
		Last Modified: Mon, 27 May 2024 16:41:02 GMT  
		Size: 34.5 MB (34498286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:51e606cd0208737194fbc3ea9cf1e32c90f2e9545bfae7c0f00f353def77f813
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30052199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c182ab0438cec99577a10b037c05f21638172ab72da06857666bb2178fc17c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:31:05 GMT
ARG RELEASE
# Mon, 27 May 2024 16:31:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:31:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:31:05 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:31:08 GMT
ADD file:37d45bf71eb61d46dd7a2368a314709dd743398ebd7e36282eac12ea29af149b in / 
# Mon, 27 May 2024 16:31:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:99b70a6005559ee2ae1c1ab75f5868065283a5a84a8ec4ef3251161922a3df4f`  
		Last Modified: Mon, 27 May 2024 16:41:08 GMT  
		Size: 30.1 MB (30052199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:e4c02475c7c9c43f8f5bf595d5260a84e1b44e49d9c5ece6d3e5dc6a0a5835a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:d86db849e59626d94f768c679aba441163c996caf7a3426f44924d0239ffe03f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5250218d28ad6612bf653eced407165dd6475a4daf9210b299fed991e172e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c90819a01d32d552ec8faf5bffc7ea2f3c9cf130ba5ce78804a07aa75a36751a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b69318504f466a22672e9fc0fcb8f4afb9d8701f88dda485c6a786bf8e3c21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:50 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:50 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:43:02 GMT
ADD file:5789980ed37544805bfc38f68255149cf4ceac7689ffcbcf606720b1b7170733 in / 
# Sat, 27 Apr 2024 14:43:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1012ed6a5d444a056b71f02e12cc46eb753d7e45477e106ebd9f6e94188a82f5`  
		Last Modified: Sat, 27 Apr 2024 14:55:09 GMT  
		Size: 23.6 MB (23623650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6edb9576e2a2080a42e4e0e9a6bc0bd91a2bf06375f9832d400bf33841d35ece
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583f1722e16e377baf906fee1ec6a9fda85ff7f3d13f536f912998601fd85ed8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ab24b025f37cc43b5958527e6fce64b2d1e36c4123010887f906d817956ae4cf
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32077140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660a3306db77bc0d9fd3510f59ecfdc664e5868e872bc91faf71f5796434f198`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:bec8a96229e24d6a9b3c333071b645c7aa7d864596ac609fbbbc89d990312394
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9374e168016e3656c0194d188dfb164fb07c23e9386799c0aec38196d359c357`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240530`

```console
$ docker pull ubuntu@sha256:d24a2b8c2facc24421e8acfa7334caa42fec6064768f42685de3f299226fb1ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20240530` - linux; amd64

```console
$ docker pull ubuntu@sha256:d86db849e59626d94f768c679aba441163c996caf7a3426f44924d0239ffe03f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5250218d28ad6612bf653eced407165dd6475a4daf9210b299fed991e172e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240530` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6edb9576e2a2080a42e4e0e9a6bc0bd91a2bf06375f9832d400bf33841d35ece
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583f1722e16e377baf906fee1ec6a9fda85ff7f3d13f536f912998601fd85ed8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240530` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ab24b025f37cc43b5958527e6fce64b2d1e36c4123010887f906d817956ae4cf
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32077140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660a3306db77bc0d9fd3510f59ecfdc664e5868e872bc91faf71f5796434f198`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240530` - linux; s390x

```console
$ docker pull ubuntu@sha256:bec8a96229e24d6a9b3c333071b645c7aa7d864596ac609fbbbc89d990312394
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9374e168016e3656c0194d188dfb164fb07c23e9386799c0aec38196d359c357`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:39ab14240b6da1cb8c34bd4f498b90b7cf3b6c6aa2d524f45c9501038d6b2709
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:94db6b944510db19c0ff5eb13281cf166abfe6f9e01a6f8e716e976664537c60
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c845845b7de8024a1ad9f6e7fd08964502a0b423aa8de631ef521863873884`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2f63021dc56651000aa1e250d42c3aa898a5cd61120aeb8daf9e7e0fd20b84e5
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26639789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0514f6822f381d7a240dfe8c419582164af5ad9465c1a95b69d1b44daedabdb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:35:06 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:35:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:35:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:35:06 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:35:17 GMT
ADD file:ab2e95a123b006ac900aaaf0d1858b88941c8d319f47e41733db6f0f5fe98b87 in / 
# Sat, 27 Apr 2024 14:35:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5b4213824fc3515b68e6844d3fc289ae00ef8cd07ddcd43856c3ad7faea16d4`  
		Last Modified: Sat, 27 Apr 2024 14:45:43 GMT  
		Size: 26.6 MB (26639789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ee2717369ac272fb83a9035762820588e77747d01a7e2fa1f36ded5a7fe672e4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27361782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442ff3b14f13ebbe3ea796b0963204140e94f9e9fc0776217cfb5a2d723fdd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8d6c06273eed7afd8e0f61334979062d373ffc7dfeb6e4a78ad8a78e688d9646
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34460693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1667f256c50ba367c051f8b8fc415211939bf5bd64beef7e4328e0fd068a5f8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:f743197c351e3d513890e8ac18fca1120555b211d848a15ecfb293cca5b31787
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95834ae443acf6a0548627723a599f867656b8f50a108c0f6375717f0c81294e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240530`

```console
$ docker pull ubuntu@sha256:5225735a99937032e871959f36d5f2a3eebf52a172408c0476605005124f3964
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20240530` - linux; amd64

```console
$ docker pull ubuntu@sha256:94db6b944510db19c0ff5eb13281cf166abfe6f9e01a6f8e716e976664537c60
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c845845b7de8024a1ad9f6e7fd08964502a0b423aa8de631ef521863873884`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240530` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ee2717369ac272fb83a9035762820588e77747d01a7e2fa1f36ded5a7fe672e4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27361782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442ff3b14f13ebbe3ea796b0963204140e94f9e9fc0776217cfb5a2d723fdd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240530` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8d6c06273eed7afd8e0f61334979062d373ffc7dfeb6e4a78ad8a78e688d9646
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34460693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1667f256c50ba367c051f8b8fc415211939bf5bd64beef7e4328e0fd068a5f8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240530` - linux; s390x

```console
$ docker pull ubuntu@sha256:f743197c351e3d513890e8ac18fca1120555b211d848a15ecfb293cca5b31787
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95834ae443acf6a0548627723a599f867656b8f50a108c0f6375717f0c81294e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:f7e60f6ed8e4233637730cf2fbcf17bd1d8855d3d25b0462637bb94efa839860
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:c279a739b31ead4ebc3e9ce04937eb8b612799b52c26133eb3b4a056d08c31a6
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28872332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c0145030df106e60e5d99149d69810db23b869ff0d3c9d236279a5a7bbb6b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00d679a470c495ef7d52e70bcd7a008f4983530b67653e63e9d3cd27fade63d7`  
		Last Modified: Thu, 30 May 2024 06:26:08 GMT  
		Size: 28.9 MB (28872332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d69717588093ca3aaa2b5721ba1b349c665417ed60509877a15538da12b73773
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26112818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f089e57ee3b8d40972824b4baff3317e5c80dcb31e0b3e79751890479a9f49`
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
```

-	Layers:
	-	`sha256:99c7292dd1d06c9e121ff292a5057d7ae7d531a72e4201db6db2e26338b60466`  
		Last Modified: Mon, 29 Apr 2024 17:08:56 GMT  
		Size: 26.1 MB (26112818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:17c24d16d63d2d089db74c2ed3e99c1ab0fd3f4f93c00b04afa8793fa793626c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28018664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc33afd4c9a541270cdae3de1f78190908ffb34081e40e636fb7fec32434e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa21f24e1940b1a682fe8effed3c9dcce0642450f7b085da08ebf725f3b70f1c`  
		Last Modified: Thu, 30 May 2024 06:26:14 GMT  
		Size: 28.0 MB (28018664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ae33d4f9381714cc1c716ccef9752aca7fcd52b5485620e8507eccd3f1a35b54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33492344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4057f9f3b277758117225481bde62f58a2690edc984fe799daa1ae9b44f11f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:059424863d1c38263ac74ee9c9b4b5d5df9febb81b7b0cd7ad14f5b351708678`  
		Last Modified: Thu, 30 May 2024 06:26:26 GMT  
		Size: 33.5 MB (33492344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:4f6b0e5e7212399168bd61c7b156c803d884b7a6dec07f387ec12cac2f2e5e86
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29167835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba52fbdc7969b516d0a34517f0853f3e95874636b88ec9e2c3d15db33cff1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dfeef248fc5b7b7a6c3c4f71a30ae3f5c8fc461af91cee39c368079dbaa3351a`  
		Last Modified: Thu, 30 May 2024 06:26:32 GMT  
		Size: 29.2 MB (29167835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:04f8e2f61d65d5f65cae9f9f88dda1c4bf72abd45de33cfb1ceda768b537ce6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic` - linux; amd64

```console
$ docker pull ubuntu@sha256:c57e8a329cd805f341ed7ee7fcc010761b29b9b8771b02a4f74fc794f1d7eac5
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27234148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77081d4f1e7217ffd2b55df73979d33fd493ad941b3c1f67f1e2364b9ee7672f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cd0bff360addc3363f9442a3e0b72ff44a74ccc0120d0fc49dfe793035242642`  
		Last Modified: Thu, 30 May 2024 04:52:39 GMT  
		Size: 27.2 MB (27234148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:76e4b6173670f4ecc21ea3264690d8c7bafd9863bd7cd2ce0f1bc4987f61bdab
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24888998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fe1df8338a7972be9f896df29e704342b3ebb3e8396f4d57844f40d2997a60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:05:53 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:05:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:05:59 GMT
ADD file:36a9fb96170feb2e8bb6dfda0793b5f7069593502c61024a6ed3d84eb01afdaf in / 
# Mon, 29 Apr 2024 16:05:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0fe43babe382dda04daea3eee6f3cad8ebf71da7df35af926aeaa07b253b2d8`  
		Last Modified: Mon, 29 Apr 2024 16:18:55 GMT  
		Size: 24.9 MB (24888998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:72c9c923b9807a752ba9c8ba41432e62bb88312de9d15b536caeaf3ea5965ad5
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26418209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ba2bc085030d6d70a7361cd2dcbfa62d90628bda1bbc5081ef895027b5f2f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9610c9b6cbed27d1798b34c30c1a9db4755a2ede67a8f5a4e9ad8821ac6afc22`  
		Last Modified: Thu, 30 May 2024 04:52:46 GMT  
		Size: 26.4 MB (26418209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:487346421a0fbd5887b0d4570b6543067670232c69d369a60626f8198a35d288
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31368685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c3391bd71baa0a068fcc1e9c12429aceeb5223ab8dee7bcc4fb7d15f57bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ec16e64158cc3af55ad7c1876c57891971c632dd2c1a37e5ffc42e9f412e13c`  
		Last Modified: Thu, 30 May 2024 04:52:59 GMT  
		Size: 31.4 MB (31368685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:d07675e241e1534e8947a5ba1895cee47b8a61643d71ec14c1e1ea8708cc47ea
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c9e0438dbf2d840e64f8c8f1ad100d0e8b7278efbd623aa303367d7e6022d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c3890b7f26f4184d913e16fb22de153b50817b714156ed910d8cc21a32a2a2df`  
		Last Modified: Thu, 30 May 2024 04:53:06 GMT  
		Size: 27.3 MB (27332665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20240530`

```console
$ docker pull ubuntu@sha256:898c71ad41430f517ee0990da586db1900e39d936d2435e10522b30df6e9475c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20240530` - linux; amd64

```console
$ docker pull ubuntu@sha256:c57e8a329cd805f341ed7ee7fcc010761b29b9b8771b02a4f74fc794f1d7eac5
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27234148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77081d4f1e7217ffd2b55df73979d33fd493ad941b3c1f67f1e2364b9ee7672f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cd0bff360addc3363f9442a3e0b72ff44a74ccc0120d0fc49dfe793035242642`  
		Last Modified: Thu, 30 May 2024 04:52:39 GMT  
		Size: 27.2 MB (27234148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240530` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:72c9c923b9807a752ba9c8ba41432e62bb88312de9d15b536caeaf3ea5965ad5
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26418209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ba2bc085030d6d70a7361cd2dcbfa62d90628bda1bbc5081ef895027b5f2f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9610c9b6cbed27d1798b34c30c1a9db4755a2ede67a8f5a4e9ad8821ac6afc22`  
		Last Modified: Thu, 30 May 2024 04:52:46 GMT  
		Size: 26.4 MB (26418209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240530` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:487346421a0fbd5887b0d4570b6543067670232c69d369a60626f8198a35d288
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31368685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c3391bd71baa0a068fcc1e9c12429aceeb5223ab8dee7bcc4fb7d15f57bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ec16e64158cc3af55ad7c1876c57891971c632dd2c1a37e5ffc42e9f412e13c`  
		Last Modified: Thu, 30 May 2024 04:52:59 GMT  
		Size: 31.4 MB (31368685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240530` - linux; s390x

```console
$ docker pull ubuntu@sha256:d07675e241e1534e8947a5ba1895cee47b8a61643d71ec14c1e1ea8708cc47ea
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27332665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c9e0438dbf2d840e64f8c8f1ad100d0e8b7278efbd623aa303367d7e6022d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c3890b7f26f4184d913e16fb22de153b50817b714156ed910d8cc21a32a2a2df`  
		Last Modified: Thu, 30 May 2024 04:53:06 GMT  
		Size: 27.3 MB (27332665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:f7e60f6ed8e4233637730cf2fbcf17bd1d8855d3d25b0462637bb94efa839860
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble` - linux; amd64

```console
$ docker pull ubuntu@sha256:c279a739b31ead4ebc3e9ce04937eb8b612799b52c26133eb3b4a056d08c31a6
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28872332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c0145030df106e60e5d99149d69810db23b869ff0d3c9d236279a5a7bbb6b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00d679a470c495ef7d52e70bcd7a008f4983530b67653e63e9d3cd27fade63d7`  
		Last Modified: Thu, 30 May 2024 06:26:08 GMT  
		Size: 28.9 MB (28872332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d69717588093ca3aaa2b5721ba1b349c665417ed60509877a15538da12b73773
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26112818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f089e57ee3b8d40972824b4baff3317e5c80dcb31e0b3e79751890479a9f49`
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
```

-	Layers:
	-	`sha256:99c7292dd1d06c9e121ff292a5057d7ae7d531a72e4201db6db2e26338b60466`  
		Last Modified: Mon, 29 Apr 2024 17:08:56 GMT  
		Size: 26.1 MB (26112818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:17c24d16d63d2d089db74c2ed3e99c1ab0fd3f4f93c00b04afa8793fa793626c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28018664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc33afd4c9a541270cdae3de1f78190908ffb34081e40e636fb7fec32434e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa21f24e1940b1a682fe8effed3c9dcce0642450f7b085da08ebf725f3b70f1c`  
		Last Modified: Thu, 30 May 2024 06:26:14 GMT  
		Size: 28.0 MB (28018664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ae33d4f9381714cc1c716ccef9752aca7fcd52b5485620e8507eccd3f1a35b54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33492344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4057f9f3b277758117225481bde62f58a2690edc984fe799daa1ae9b44f11f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:059424863d1c38263ac74ee9c9b4b5d5df9febb81b7b0cd7ad14f5b351708678`  
		Last Modified: Thu, 30 May 2024 06:26:26 GMT  
		Size: 33.5 MB (33492344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:4f6b0e5e7212399168bd61c7b156c803d884b7a6dec07f387ec12cac2f2e5e86
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29167835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba52fbdc7969b516d0a34517f0853f3e95874636b88ec9e2c3d15db33cff1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dfeef248fc5b7b7a6c3c4f71a30ae3f5c8fc461af91cee39c368079dbaa3351a`  
		Last Modified: Thu, 30 May 2024 06:26:32 GMT  
		Size: 29.2 MB (29167835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240530`

```console
$ docker pull ubuntu@sha256:61d059dacc2f55cfa9654130d32b7640f86c68b4523a2141f64294e625f6032a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble-20240530` - linux; amd64

```console
$ docker pull ubuntu@sha256:c279a739b31ead4ebc3e9ce04937eb8b612799b52c26133eb3b4a056d08c31a6
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28872332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c0145030df106e60e5d99149d69810db23b869ff0d3c9d236279a5a7bbb6b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00d679a470c495ef7d52e70bcd7a008f4983530b67653e63e9d3cd27fade63d7`  
		Last Modified: Thu, 30 May 2024 06:26:08 GMT  
		Size: 28.9 MB (28872332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240530` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:17c24d16d63d2d089db74c2ed3e99c1ab0fd3f4f93c00b04afa8793fa793626c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28018664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc33afd4c9a541270cdae3de1f78190908ffb34081e40e636fb7fec32434e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa21f24e1940b1a682fe8effed3c9dcce0642450f7b085da08ebf725f3b70f1c`  
		Last Modified: Thu, 30 May 2024 06:26:14 GMT  
		Size: 28.0 MB (28018664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240530` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ae33d4f9381714cc1c716ccef9752aca7fcd52b5485620e8507eccd3f1a35b54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33492344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4057f9f3b277758117225481bde62f58a2690edc984fe799daa1ae9b44f11f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:059424863d1c38263ac74ee9c9b4b5d5df9febb81b7b0cd7ad14f5b351708678`  
		Last Modified: Thu, 30 May 2024 06:26:26 GMT  
		Size: 33.5 MB (33492344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240530` - linux; s390x

```console
$ docker pull ubuntu@sha256:4f6b0e5e7212399168bd61c7b156c803d884b7a6dec07f387ec12cac2f2e5e86
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29167835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba52fbdc7969b516d0a34517f0853f3e95874636b88ec9e2c3d15db33cff1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dfeef248fc5b7b7a6c3c4f71a30ae3f5c8fc461af91cee39c368079dbaa3351a`  
		Last Modified: Thu, 30 May 2024 06:26:32 GMT  
		Size: 29.2 MB (29167835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:oracular`

```console
$ docker pull ubuntu@sha256:4cfc6f38ba7d6bdbacd66b7877013b54193e8bf89ce9d31742b6a7ff5d3ccb7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:oracular` - linux; amd64

```console
$ docker pull ubuntu@sha256:f0e91d9bc9a7a5bea3bb3a985f790da4c54b8a71459b9a05889b8bca94136dce
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29771141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195922705d1ac968c7a2957347fb5dcfab18beeb51127d9857538cbd1385d23d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:26:46 GMT
ARG RELEASE
# Mon, 27 May 2024 16:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:26:47 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:26:48 GMT
ADD file:7494747de214fc382e1eb68d321438cc6d5867ef746ee5d62919406473341936 in / 
# Mon, 27 May 2024 16:26:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ef7bc4a68771f815262911dbd473dbd9fcd723dcfd13a33b1d0a260a29e9825d`  
		Last Modified: Mon, 27 May 2024 16:40:43 GMT  
		Size: 29.8 MB (29771141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6015d5cffae622f7779768d05d3f86be6663b53f3e71c5f15878c12cdb19dbe0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28888016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39255a8b34c94b48a216a3a04ffb909fdbdcfaa99b33562e7e5a631dea13d6e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:29:14 GMT
ARG RELEASE
# Mon, 27 May 2024 16:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:29:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:29:14 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:29:21 GMT
ADD file:58d1f4adeda18acaf194d00b71d74450c8fbd68230273d1f50b8c0dd22799461 in / 
# Mon, 27 May 2024 16:29:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca17094f6427bbffbfb5aa37095119c9ff0e754728b899b6364837de4f71deef`  
		Last Modified: Mon, 27 May 2024 16:40:49 GMT  
		Size: 28.9 MB (28888016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:4ba709a557c76c77df139e664c1fda668f0298d49513b21fffca19384bf64233
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34498286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2718335dd3099fca397f699ba7511d175af30e6649ea9978052fbb9109b8b345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:23:19 GMT
ARG RELEASE
# Mon, 27 May 2024 16:23:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:23:19 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:23:23 GMT
ADD file:19080182caa6d088e7b16cfb92ba73313501dd5937d3d756cfde855b0419151e in / 
# Mon, 27 May 2024 16:23:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95deb0d73890be47bc15a9488fe4038e8df63561527f7d9715cff885b11314f7`  
		Last Modified: Mon, 27 May 2024 16:41:02 GMT  
		Size: 34.5 MB (34498286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; s390x

```console
$ docker pull ubuntu@sha256:51e606cd0208737194fbc3ea9cf1e32c90f2e9545bfae7c0f00f353def77f813
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30052199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c182ab0438cec99577a10b037c05f21638172ab72da06857666bb2178fc17c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:31:05 GMT
ARG RELEASE
# Mon, 27 May 2024 16:31:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:31:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:31:05 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:31:08 GMT
ADD file:37d45bf71eb61d46dd7a2368a314709dd743398ebd7e36282eac12ea29af149b in / 
# Mon, 27 May 2024 16:31:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:99b70a6005559ee2ae1c1ab75f5868065283a5a84a8ec4ef3251161922a3df4f`  
		Last Modified: Mon, 27 May 2024 16:41:08 GMT  
		Size: 30.1 MB (30052199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:oracular-20240527`

```console
$ docker pull ubuntu@sha256:4cfc6f38ba7d6bdbacd66b7877013b54193e8bf89ce9d31742b6a7ff5d3ccb7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:oracular-20240527` - linux; amd64

```console
$ docker pull ubuntu@sha256:f0e91d9bc9a7a5bea3bb3a985f790da4c54b8a71459b9a05889b8bca94136dce
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29771141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195922705d1ac968c7a2957347fb5dcfab18beeb51127d9857538cbd1385d23d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:26:46 GMT
ARG RELEASE
# Mon, 27 May 2024 16:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:26:47 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:26:48 GMT
ADD file:7494747de214fc382e1eb68d321438cc6d5867ef746ee5d62919406473341936 in / 
# Mon, 27 May 2024 16:26:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ef7bc4a68771f815262911dbd473dbd9fcd723dcfd13a33b1d0a260a29e9825d`  
		Last Modified: Mon, 27 May 2024 16:40:43 GMT  
		Size: 29.8 MB (29771141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240527` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6015d5cffae622f7779768d05d3f86be6663b53f3e71c5f15878c12cdb19dbe0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28888016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39255a8b34c94b48a216a3a04ffb909fdbdcfaa99b33562e7e5a631dea13d6e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:29:14 GMT
ARG RELEASE
# Mon, 27 May 2024 16:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:29:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:29:14 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:29:21 GMT
ADD file:58d1f4adeda18acaf194d00b71d74450c8fbd68230273d1f50b8c0dd22799461 in / 
# Mon, 27 May 2024 16:29:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca17094f6427bbffbfb5aa37095119c9ff0e754728b899b6364837de4f71deef`  
		Last Modified: Mon, 27 May 2024 16:40:49 GMT  
		Size: 28.9 MB (28888016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240527` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:4ba709a557c76c77df139e664c1fda668f0298d49513b21fffca19384bf64233
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34498286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2718335dd3099fca397f699ba7511d175af30e6649ea9978052fbb9109b8b345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:23:19 GMT
ARG RELEASE
# Mon, 27 May 2024 16:23:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:23:19 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:23:23 GMT
ADD file:19080182caa6d088e7b16cfb92ba73313501dd5937d3d756cfde855b0419151e in / 
# Mon, 27 May 2024 16:23:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95deb0d73890be47bc15a9488fe4038e8df63561527f7d9715cff885b11314f7`  
		Last Modified: Mon, 27 May 2024 16:41:02 GMT  
		Size: 34.5 MB (34498286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240527` - linux; s390x

```console
$ docker pull ubuntu@sha256:51e606cd0208737194fbc3ea9cf1e32c90f2e9545bfae7c0f00f353def77f813
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30052199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c182ab0438cec99577a10b037c05f21638172ab72da06857666bb2178fc17c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:31:05 GMT
ARG RELEASE
# Mon, 27 May 2024 16:31:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:31:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:31:05 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:31:08 GMT
ADD file:37d45bf71eb61d46dd7a2368a314709dd743398ebd7e36282eac12ea29af149b in / 
# Mon, 27 May 2024 16:31:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:99b70a6005559ee2ae1c1ab75f5868065283a5a84a8ec4ef3251161922a3df4f`  
		Last Modified: Mon, 27 May 2024 16:41:08 GMT  
		Size: 30.1 MB (30052199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:f7e60f6ed8e4233637730cf2fbcf17bd1d8855d3d25b0462637bb94efa839860
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
$ docker pull ubuntu@sha256:c279a739b31ead4ebc3e9ce04937eb8b612799b52c26133eb3b4a056d08c31a6
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28872332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c0145030df106e60e5d99149d69810db23b869ff0d3c9d236279a5a7bbb6b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00d679a470c495ef7d52e70bcd7a008f4983530b67653e63e9d3cd27fade63d7`  
		Last Modified: Thu, 30 May 2024 06:26:08 GMT  
		Size: 28.9 MB (28872332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d69717588093ca3aaa2b5721ba1b349c665417ed60509877a15538da12b73773
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26112818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f089e57ee3b8d40972824b4baff3317e5c80dcb31e0b3e79751890479a9f49`
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
```

-	Layers:
	-	`sha256:99c7292dd1d06c9e121ff292a5057d7ae7d531a72e4201db6db2e26338b60466`  
		Last Modified: Mon, 29 Apr 2024 17:08:56 GMT  
		Size: 26.1 MB (26112818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:17c24d16d63d2d089db74c2ed3e99c1ab0fd3f4f93c00b04afa8793fa793626c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28018664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc33afd4c9a541270cdae3de1f78190908ffb34081e40e636fb7fec32434e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa21f24e1940b1a682fe8effed3c9dcce0642450f7b085da08ebf725f3b70f1c`  
		Last Modified: Thu, 30 May 2024 06:26:14 GMT  
		Size: 28.0 MB (28018664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ae33d4f9381714cc1c716ccef9752aca7fcd52b5485620e8507eccd3f1a35b54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33492344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4057f9f3b277758117225481bde62f58a2690edc984fe799daa1ae9b44f11f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:059424863d1c38263ac74ee9c9b4b5d5df9febb81b7b0cd7ad14f5b351708678`  
		Last Modified: Thu, 30 May 2024 06:26:26 GMT  
		Size: 33.5 MB (33492344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:4f6b0e5e7212399168bd61c7b156c803d884b7a6dec07f387ec12cac2f2e5e86
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29167835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba52fbdc7969b516d0a34517f0853f3e95874636b88ec9e2c3d15db33cff1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dfeef248fc5b7b7a6c3c4f71a30ae3f5c8fc461af91cee39c368079dbaa3351a`  
		Last Modified: Thu, 30 May 2024 06:26:32 GMT  
		Size: 29.2 MB (29167835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
