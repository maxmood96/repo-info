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
-	[`ubuntu:noble-20240605`](#ubuntunoble-20240605)
-	[`ubuntu:oracular`](#ubuntuoracular)
-	[`ubuntu:oracular-20240527`](#ubuntuoracular-20240527)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:0b897358ff6624825fb50d20ffb605ab0eaea77ced0adb8c6a4b756513dec6fc
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
$ docker pull ubuntu@sha256:717a8dabf82777782587740c79fd8704d3ec06583be6eacc67242cd00b9a0fd1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b0680c06e6c394ed258bc7929b97e1bdf910e0b7f128b98d5e332363e570e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
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
$ docker pull ubuntu@sha256:19478ce7fc2ffbce89df29fea5725a8d12e57de52eb9ea570890dc5852aac1ac
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
$ docker pull ubuntu@sha256:d3009406bbc0442a943ae92203a36760a55ccbac4dd48bae07384c053fe5678f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26639042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a727e65b3d1d389d62567af457d15c696e6f80b79ca0b0484ae71abe7e08bf7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7d6949ac966fed9a061428466d68cc616d739583d012661c3c826f017b64981`  
		Last Modified: Mon, 03 Jun 2024 10:46:59 GMT  
		Size: 26.6 MB (26639042 bytes)  
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
$ docker pull ubuntu@sha256:fd7fe639db24c4e005643921beea92bc449aac4f4d40d60cd9ad9ab6456aec01
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
$ docker pull ubuntu@sha256:1b6bcf792688b1785446e313362693c258430e5f2868d9f6b7369fa545410ce4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24889640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3794c41d97830edf2fb23a4bf73adb8402fd53da962e372711d294b4a0228cba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:02bc623595c9855bd7f40991602742e9c62515b4c2d290f04f6bb9cbc72f4eb6`  
		Last Modified: Thu, 30 May 2024 04:52:52 GMT  
		Size: 24.9 MB (24889640 bytes)  
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
$ docker pull ubuntu@sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
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
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a3b5c0d95b7ce708cd05f3d254e093f1b53ea1c699f1d5a0c76743e683c9eaa2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34506029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66e343649a1106ba7e8df5679410ec0497411fbdb4ba5c4c5da74da68e56f46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.10`

```console
$ docker pull ubuntu@sha256:1cb75bbc36738eec8f60ae12d71cd3a191bf4e6256f2fd5706bd8480257d0cee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
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

### `ubuntu:24.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:72f71bfb60bcacc7509e8706eb8ba1d1c65c6efcc4904341445de07a8da4384d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26885350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e619c032c2db72ec27395a57472292e2a31de07619b6916a1d3a75ff2ae7c0b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:26:46 GMT
ARG RELEASE
# Mon, 27 May 2024 16:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:26:53 GMT
ADD file:a40794020d6cd46817b1b48ec5173ba956c8914b10e64764dcc5c2f15e457628 in / 
# Mon, 27 May 2024 16:26:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:965182ec5c69ae9b4e13dba3a63646d87963cf3ecb09119c6fb41ac6833f5735`  
		Last Modified: Mon, 27 May 2024 16:40:55 GMT  
		Size: 26.9 MB (26885350 bytes)  
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
$ docker pull ubuntu@sha256:1cb75bbc36738eec8f60ae12d71cd3a191bf4e6256f2fd5706bd8480257d0cee
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
$ docker pull ubuntu@sha256:72f71bfb60bcacc7509e8706eb8ba1d1c65c6efcc4904341445de07a8da4384d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26885350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e619c032c2db72ec27395a57472292e2a31de07619b6916a1d3a75ff2ae7c0b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:26:46 GMT
ARG RELEASE
# Mon, 27 May 2024 16:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:26:53 GMT
ADD file:a40794020d6cd46817b1b48ec5173ba956c8914b10e64764dcc5c2f15e457628 in / 
# Mon, 27 May 2024 16:26:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:965182ec5c69ae9b4e13dba3a63646d87963cf3ecb09119c6fb41ac6833f5735`  
		Last Modified: Mon, 27 May 2024 16:40:55 GMT  
		Size: 26.9 MB (26885350 bytes)  
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
$ docker pull ubuntu@sha256:0b897358ff6624825fb50d20ffb605ab0eaea77ced0adb8c6a4b756513dec6fc
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
$ docker pull ubuntu@sha256:717a8dabf82777782587740c79fd8704d3ec06583be6eacc67242cd00b9a0fd1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b0680c06e6c394ed258bc7929b97e1bdf910e0b7f128b98d5e332363e570e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
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
$ docker pull ubuntu@sha256:0b897358ff6624825fb50d20ffb605ab0eaea77ced0adb8c6a4b756513dec6fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
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

### `ubuntu:focal-20240530` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:717a8dabf82777782587740c79fd8704d3ec06583be6eacc67242cd00b9a0fd1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b0680c06e6c394ed258bc7929b97e1bdf910e0b7f128b98d5e332363e570e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
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
$ docker pull ubuntu@sha256:19478ce7fc2ffbce89df29fea5725a8d12e57de52eb9ea570890dc5852aac1ac
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
$ docker pull ubuntu@sha256:d3009406bbc0442a943ae92203a36760a55ccbac4dd48bae07384c053fe5678f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26639042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a727e65b3d1d389d62567af457d15c696e6f80b79ca0b0484ae71abe7e08bf7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7d6949ac966fed9a061428466d68cc616d739583d012661c3c826f017b64981`  
		Last Modified: Mon, 03 Jun 2024 10:46:59 GMT  
		Size: 26.6 MB (26639042 bytes)  
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
$ docker pull ubuntu@sha256:19478ce7fc2ffbce89df29fea5725a8d12e57de52eb9ea570890dc5852aac1ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
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

### `ubuntu:jammy-20240530` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d3009406bbc0442a943ae92203a36760a55ccbac4dd48bae07384c053fe5678f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26639042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a727e65b3d1d389d62567af457d15c696e6f80b79ca0b0484ae71abe7e08bf7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:36:14 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:36:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:36:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:36:23 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 03 Jun 2024 10:36:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7d6949ac966fed9a061428466d68cc616d739583d012661c3c826f017b64981`  
		Last Modified: Mon, 03 Jun 2024 10:46:59 GMT  
		Size: 26.6 MB (26639042 bytes)  
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
$ docker pull ubuntu@sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
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
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a3b5c0d95b7ce708cd05f3d254e093f1b53ea1c699f1d5a0c76743e683c9eaa2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34506029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66e343649a1106ba7e8df5679410ec0497411fbdb4ba5c4c5da74da68e56f46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:fd7fe639db24c4e005643921beea92bc449aac4f4d40d60cd9ad9ab6456aec01
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
$ docker pull ubuntu@sha256:1b6bcf792688b1785446e313362693c258430e5f2868d9f6b7369fa545410ce4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24889640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3794c41d97830edf2fb23a4bf73adb8402fd53da962e372711d294b4a0228cba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:02bc623595c9855bd7f40991602742e9c62515b4c2d290f04f6bb9cbc72f4eb6`  
		Last Modified: Thu, 30 May 2024 04:52:52 GMT  
		Size: 24.9 MB (24889640 bytes)  
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
$ docker pull ubuntu@sha256:fd7fe639db24c4e005643921beea92bc449aac4f4d40d60cd9ad9ab6456aec01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
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

### `ubuntu:mantic-20240530` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1b6bcf792688b1785446e313362693c258430e5f2868d9f6b7369fa545410ce4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24889640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3794c41d97830edf2fb23a4bf73adb8402fd53da962e372711d294b4a0228cba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:02bc623595c9855bd7f40991602742e9c62515b4c2d290f04f6bb9cbc72f4eb6`  
		Last Modified: Thu, 30 May 2024 04:52:52 GMT  
		Size: 24.9 MB (24889640 bytes)  
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
$ docker pull ubuntu@sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
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
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a3b5c0d95b7ce708cd05f3d254e093f1b53ea1c699f1d5a0c76743e683c9eaa2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34506029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66e343649a1106ba7e8df5679410ec0497411fbdb4ba5c4c5da74da68e56f46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240605`

```console
$ docker pull ubuntu@sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble-20240605` - linux; amd64

```console
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240605` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240605` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240605` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a3b5c0d95b7ce708cd05f3d254e093f1b53ea1c699f1d5a0c76743e683c9eaa2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34506029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66e343649a1106ba7e8df5679410ec0497411fbdb4ba5c4c5da74da68e56f46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240605` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:oracular`

```console
$ docker pull ubuntu@sha256:1cb75bbc36738eec8f60ae12d71cd3a191bf4e6256f2fd5706bd8480257d0cee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
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

### `ubuntu:oracular` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:72f71bfb60bcacc7509e8706eb8ba1d1c65c6efcc4904341445de07a8da4384d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26885350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e619c032c2db72ec27395a57472292e2a31de07619b6916a1d3a75ff2ae7c0b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:26:46 GMT
ARG RELEASE
# Mon, 27 May 2024 16:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:26:53 GMT
ADD file:a40794020d6cd46817b1b48ec5173ba956c8914b10e64764dcc5c2f15e457628 in / 
# Mon, 27 May 2024 16:26:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:965182ec5c69ae9b4e13dba3a63646d87963cf3ecb09119c6fb41ac6833f5735`  
		Last Modified: Mon, 27 May 2024 16:40:55 GMT  
		Size: 26.9 MB (26885350 bytes)  
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
$ docker pull ubuntu@sha256:1cb75bbc36738eec8f60ae12d71cd3a191bf4e6256f2fd5706bd8480257d0cee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
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

### `ubuntu:oracular-20240527` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:72f71bfb60bcacc7509e8706eb8ba1d1c65c6efcc4904341445de07a8da4384d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26885350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e619c032c2db72ec27395a57472292e2a31de07619b6916a1d3a75ff2ae7c0b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 May 2024 16:26:46 GMT
ARG RELEASE
# Mon, 27 May 2024 16:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 16:26:46 GMT
LABEL org.opencontainers.image.version=24.10
# Mon, 27 May 2024 16:26:53 GMT
ADD file:a40794020d6cd46817b1b48ec5173ba956c8914b10e64764dcc5c2f15e457628 in / 
# Mon, 27 May 2024 16:26:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:965182ec5c69ae9b4e13dba3a63646d87963cf3ecb09119c6fb41ac6833f5735`  
		Last Modified: Mon, 27 May 2024 16:40:55 GMT  
		Size: 26.9 MB (26885350 bytes)  
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
$ docker pull ubuntu@sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
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
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a3b5c0d95b7ce708cd05f3d254e093f1b53ea1c699f1d5a0c76743e683c9eaa2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34506029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66e343649a1106ba7e8df5679410ec0497411fbdb4ba5c4c5da74da68e56f46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
