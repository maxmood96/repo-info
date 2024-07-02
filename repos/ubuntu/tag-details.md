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
-	[`ubuntu:jammy-20240627.1`](#ubuntujammy-202406271)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20240530`](#ubuntumantic-20240530)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240605`](#ubuntunoble-20240605)
-	[`ubuntu:oracular`](#ubuntuoracular)
-	[`ubuntu:oracular-20240617`](#ubuntuoracular-20240617)
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
$ docker pull ubuntu@sha256:340d9b015b194dc6e2a13938944e0d016e57b9679963fdeb9ce021daac430221
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
$ docker pull ubuntu@sha256:0eb0f877e1c869a300c442c41120e778db7161419244ee5cbc6fa5f134e74736
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3cdc4d1ad3e314a91f76b7b99eed443f2152e3a9bf33e46669b31d094be443`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e215e52905ebb967da009a009b681f219e456122d4382a370b0c7d56c21c7bb8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0de33827595e70e002da57b43f06ee3bbef7f7418dd4edcd8e402aba2011dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f6d2cceb710e897ef3b81e28ea21268aa6d28deae90ac1ab9602ff738c88a650`  
		Last Modified: Thu, 27 Jun 2024 20:18:40 GMT  
		Size: 26.6 MB (26638444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d19c776e76cdb32dcc72cbd44a689c9be9518b9c4ed7f9a92b38f46176b931b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27360025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04dcc2ab57b0d5d6e9d3d9c65f899d400d14114dace7a30acc84f36bb609cdd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:734892385eba098d7c7726ff2f2918c959a346020f9ba36153878d401c907989
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34461081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b62ef115c503831839d8467dfe7f7d59c6ac82924643e86212bd410695a0744`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:01c176682053467414f35141cdc9da3c40a340eba1f0d3a928e4e52d021fa5f9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611e60cc7007d67350be72fec6adb06b36ffa3f04bac4400b7ca37107acf9cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
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
$ docker pull ubuntu@sha256:1367c15864fc79b5c8ba6be301c83ec2bccf5c1b4a53af71793f740e194598fd
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
$ docker pull ubuntu@sha256:2a1e42397521001f21178a06e37ba1024481d3e8b6a754902ac5fb6a0861c7ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29784075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94351b6d67ec74ba3dbc8816e783fd62253ef818a920616c0e6142348af486c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:32 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:34 GMT
ADD file:7de44056586ca78e2d663ff6f13ed78bd93df3759032c25b398020b7f7a508e9 in / 
# Tue, 18 Jun 2024 11:55:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:044e986ad11c8558c1ced47a645123223d7169e0603217f6b5810ae6d5ed8990`  
		Last Modified: Tue, 18 Jun 2024 12:05:48 GMT  
		Size: 29.8 MB (29784075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:454de8793a5d34b0dee0dbd13719a2c6eeadd7944bacdcace19263cbe9b3a94e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26906015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c89d5967405dc83e44998f274cee92367c1a5535fedf5b28786b266541ed4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:40 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:46 GMT
ADD file:c13178f5cbf3534e02829f373860ffe37af2e84d45812bd7eabc39b4e79bf01a in / 
# Tue, 18 Jun 2024 11:55:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26cb78abf3e6e59cb1ecc37a2ce7bfa44b6eea15ae8bd75ae12a67b744fb8a14`  
		Last Modified: Tue, 18 Jun 2024 12:06:00 GMT  
		Size: 26.9 MB (26906015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0f58dd64e1e2b1f2c96e2b2cab30402540724a399061b035051534808114144a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28910084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098a556a9a5dea3e4f745912c1182f1a25e8814ed8f855b4221bd99bb15e0d61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:34 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:40 GMT
ADD file:34ce123f3395299e473794d0c46e368375bf7c9630a67258382f114f83a82c40 in / 
# Tue, 18 Jun 2024 11:55:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8fecd43832f92adee10b7b226a92bb3186239d955e0f1d97d8239791a46784fe`  
		Last Modified: Tue, 18 Jun 2024 12:05:54 GMT  
		Size: 28.9 MB (28910084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ab0729c8fa6a0ab6a3eb07d31438b079e5823107c47b40bffdf8d6c23d5ea542
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34468676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a867e4f4fc9ad515223d70da1936dc4715dfc470d5b12767ef2e5a0bc1cac43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 10:39:06 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:39:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:39:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:39:06 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 10:39:10 GMT
ADD file:3a2687ed020c5070cf555af85025ee8ecf7891a467a2e7122bbeba895861d0b0 in / 
# Tue, 18 Jun 2024 10:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e5aa51133e1c5d213e45194cbadfbfe99c6a335d3391eb4068a9a4f71a4d9c68`  
		Last Modified: Tue, 18 Jun 2024 12:06:07 GMT  
		Size: 34.5 MB (34468676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:579f926bf5b5737bb4a6e7a96a26b972ff53efd0e897ca6ad60a5177f646fc23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30020524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acda71050f1c0d987f22287e80bf0f8d8053b3603156d7110c4c8ac85ce1d13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:36 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:39 GMT
ADD file:4bdbaa8c03466d03a76656bbdf683d02b08207350051e5d5d8d46f60ae2ebffd in / 
# Tue, 18 Jun 2024 11:55:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92821b1303c5ddcb3e722c91af39dfee67d938dade7d06501348340be1bafc4b`  
		Last Modified: Tue, 18 Jun 2024 12:06:20 GMT  
		Size: 30.0 MB (30020524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:b7c7d0b22ba1052e2cce660c2f559bb9ea42ad1220c9cc467bc9fb49eca5b202
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:2a1e42397521001f21178a06e37ba1024481d3e8b6a754902ac5fb6a0861c7ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29784075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94351b6d67ec74ba3dbc8816e783fd62253ef818a920616c0e6142348af486c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:32 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:34 GMT
ADD file:7de44056586ca78e2d663ff6f13ed78bd93df3759032c25b398020b7f7a508e9 in / 
# Tue, 18 Jun 2024 11:55:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:044e986ad11c8558c1ced47a645123223d7169e0603217f6b5810ae6d5ed8990`  
		Last Modified: Tue, 18 Jun 2024 12:05:48 GMT  
		Size: 29.8 MB (29784075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:454de8793a5d34b0dee0dbd13719a2c6eeadd7944bacdcace19263cbe9b3a94e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26906015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c89d5967405dc83e44998f274cee92367c1a5535fedf5b28786b266541ed4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:40 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:46 GMT
ADD file:c13178f5cbf3534e02829f373860ffe37af2e84d45812bd7eabc39b4e79bf01a in / 
# Tue, 18 Jun 2024 11:55:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26cb78abf3e6e59cb1ecc37a2ce7bfa44b6eea15ae8bd75ae12a67b744fb8a14`  
		Last Modified: Tue, 18 Jun 2024 12:06:00 GMT  
		Size: 26.9 MB (26906015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0f58dd64e1e2b1f2c96e2b2cab30402540724a399061b035051534808114144a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28910084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098a556a9a5dea3e4f745912c1182f1a25e8814ed8f855b4221bd99bb15e0d61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:34 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:40 GMT
ADD file:34ce123f3395299e473794d0c46e368375bf7c9630a67258382f114f83a82c40 in / 
# Tue, 18 Jun 2024 11:55:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8fecd43832f92adee10b7b226a92bb3186239d955e0f1d97d8239791a46784fe`  
		Last Modified: Tue, 18 Jun 2024 12:05:54 GMT  
		Size: 28.9 MB (28910084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ab0729c8fa6a0ab6a3eb07d31438b079e5823107c47b40bffdf8d6c23d5ea542
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34468676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a867e4f4fc9ad515223d70da1936dc4715dfc470d5b12767ef2e5a0bc1cac43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 10:39:06 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:39:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:39:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:39:06 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 10:39:10 GMT
ADD file:3a2687ed020c5070cf555af85025ee8ecf7891a467a2e7122bbeba895861d0b0 in / 
# Tue, 18 Jun 2024 10:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e5aa51133e1c5d213e45194cbadfbfe99c6a335d3391eb4068a9a4f71a4d9c68`  
		Last Modified: Tue, 18 Jun 2024 12:06:07 GMT  
		Size: 34.5 MB (34468676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; riscv64

```console
$ docker pull ubuntu@sha256:d19ba26eb53b3b5d6553756a420cbd4b15b5cea0b53af9899f2ada01174745ee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25669058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fdb55215bb484783ea45c3ba874a9b8886993abb3cb25be7d6ae2bd128b126`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:09:01 GMT
ADD file:512505c2df26db88aeeb5025ff073a2d8e98d995422df61a5cad94d79ef22a42 in / 
# Mon, 02 Jan 2023 18:09:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ada5e428c090bd736690979612e7bece7c31ff1f1701ca35de4d1899e835e69a`  
		Last Modified: Mon, 02 Jan 2023 18:09:56 GMT  
		Size: 25.7 MB (25669058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:579f926bf5b5737bb4a6e7a96a26b972ff53efd0e897ca6ad60a5177f646fc23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30020524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acda71050f1c0d987f22287e80bf0f8d8053b3603156d7110c4c8ac85ce1d13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:36 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:39 GMT
ADD file:4bdbaa8c03466d03a76656bbdf683d02b08207350051e5d5d8d46f60ae2ebffd in / 
# Tue, 18 Jun 2024 11:55:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92821b1303c5ddcb3e722c91af39dfee67d938dade7d06501348340be1bafc4b`  
		Last Modified: Tue, 18 Jun 2024 12:06:20 GMT  
		Size: 30.0 MB (30020524 bytes)  
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
$ docker pull ubuntu@sha256:340d9b015b194dc6e2a13938944e0d016e57b9679963fdeb9ce021daac430221
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
$ docker pull ubuntu@sha256:0eb0f877e1c869a300c442c41120e778db7161419244ee5cbc6fa5f134e74736
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3cdc4d1ad3e314a91f76b7b99eed443f2152e3a9bf33e46669b31d094be443`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e215e52905ebb967da009a009b681f219e456122d4382a370b0c7d56c21c7bb8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0de33827595e70e002da57b43f06ee3bbef7f7418dd4edcd8e402aba2011dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f6d2cceb710e897ef3b81e28ea21268aa6d28deae90ac1ab9602ff738c88a650`  
		Last Modified: Thu, 27 Jun 2024 20:18:40 GMT  
		Size: 26.6 MB (26638444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d19c776e76cdb32dcc72cbd44a689c9be9518b9c4ed7f9a92b38f46176b931b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27360025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04dcc2ab57b0d5d6e9d3d9c65f899d400d14114dace7a30acc84f36bb609cdd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:734892385eba098d7c7726ff2f2918c959a346020f9ba36153878d401c907989
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34461081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b62ef115c503831839d8467dfe7f7d59c6ac82924643e86212bd410695a0744`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:01c176682053467414f35141cdc9da3c40a340eba1f0d3a928e4e52d021fa5f9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611e60cc7007d67350be72fec6adb06b36ffa3f04bac4400b7ca37107acf9cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240627.1`

```console
$ docker pull ubuntu@sha256:340d9b015b194dc6e2a13938944e0d016e57b9679963fdeb9ce021daac430221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20240627.1` - linux; amd64

```console
$ docker pull ubuntu@sha256:0eb0f877e1c869a300c442c41120e778db7161419244ee5cbc6fa5f134e74736
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3cdc4d1ad3e314a91f76b7b99eed443f2152e3a9bf33e46669b31d094be443`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240627.1` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e215e52905ebb967da009a009b681f219e456122d4382a370b0c7d56c21c7bb8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0de33827595e70e002da57b43f06ee3bbef7f7418dd4edcd8e402aba2011dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f6d2cceb710e897ef3b81e28ea21268aa6d28deae90ac1ab9602ff738c88a650`  
		Last Modified: Thu, 27 Jun 2024 20:18:40 GMT  
		Size: 26.6 MB (26638444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240627.1` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d19c776e76cdb32dcc72cbd44a689c9be9518b9c4ed7f9a92b38f46176b931b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27360025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04dcc2ab57b0d5d6e9d3d9c65f899d400d14114dace7a30acc84f36bb609cdd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240627.1` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:734892385eba098d7c7726ff2f2918c959a346020f9ba36153878d401c907989
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34461081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b62ef115c503831839d8467dfe7f7d59c6ac82924643e86212bd410695a0744`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240627.1` - linux; s390x

```console
$ docker pull ubuntu@sha256:01c176682053467414f35141cdc9da3c40a340eba1f0d3a928e4e52d021fa5f9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611e60cc7007d67350be72fec6adb06b36ffa3f04bac4400b7ca37107acf9cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
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
$ docker pull ubuntu@sha256:1367c15864fc79b5c8ba6be301c83ec2bccf5c1b4a53af71793f740e194598fd
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
$ docker pull ubuntu@sha256:2a1e42397521001f21178a06e37ba1024481d3e8b6a754902ac5fb6a0861c7ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29784075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94351b6d67ec74ba3dbc8816e783fd62253ef818a920616c0e6142348af486c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:32 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:34 GMT
ADD file:7de44056586ca78e2d663ff6f13ed78bd93df3759032c25b398020b7f7a508e9 in / 
# Tue, 18 Jun 2024 11:55:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:044e986ad11c8558c1ced47a645123223d7169e0603217f6b5810ae6d5ed8990`  
		Last Modified: Tue, 18 Jun 2024 12:05:48 GMT  
		Size: 29.8 MB (29784075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:454de8793a5d34b0dee0dbd13719a2c6eeadd7944bacdcace19263cbe9b3a94e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26906015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c89d5967405dc83e44998f274cee92367c1a5535fedf5b28786b266541ed4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:40 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:46 GMT
ADD file:c13178f5cbf3534e02829f373860ffe37af2e84d45812bd7eabc39b4e79bf01a in / 
# Tue, 18 Jun 2024 11:55:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26cb78abf3e6e59cb1ecc37a2ce7bfa44b6eea15ae8bd75ae12a67b744fb8a14`  
		Last Modified: Tue, 18 Jun 2024 12:06:00 GMT  
		Size: 26.9 MB (26906015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0f58dd64e1e2b1f2c96e2b2cab30402540724a399061b035051534808114144a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28910084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098a556a9a5dea3e4f745912c1182f1a25e8814ed8f855b4221bd99bb15e0d61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:34 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:40 GMT
ADD file:34ce123f3395299e473794d0c46e368375bf7c9630a67258382f114f83a82c40 in / 
# Tue, 18 Jun 2024 11:55:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8fecd43832f92adee10b7b226a92bb3186239d955e0f1d97d8239791a46784fe`  
		Last Modified: Tue, 18 Jun 2024 12:05:54 GMT  
		Size: 28.9 MB (28910084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ab0729c8fa6a0ab6a3eb07d31438b079e5823107c47b40bffdf8d6c23d5ea542
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34468676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a867e4f4fc9ad515223d70da1936dc4715dfc470d5b12767ef2e5a0bc1cac43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 10:39:06 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:39:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:39:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:39:06 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 10:39:10 GMT
ADD file:3a2687ed020c5070cf555af85025ee8ecf7891a467a2e7122bbeba895861d0b0 in / 
# Tue, 18 Jun 2024 10:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e5aa51133e1c5d213e45194cbadfbfe99c6a335d3391eb4068a9a4f71a4d9c68`  
		Last Modified: Tue, 18 Jun 2024 12:06:07 GMT  
		Size: 34.5 MB (34468676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; s390x

```console
$ docker pull ubuntu@sha256:579f926bf5b5737bb4a6e7a96a26b972ff53efd0e897ca6ad60a5177f646fc23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30020524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acda71050f1c0d987f22287e80bf0f8d8053b3603156d7110c4c8ac85ce1d13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:36 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:39 GMT
ADD file:4bdbaa8c03466d03a76656bbdf683d02b08207350051e5d5d8d46f60ae2ebffd in / 
# Tue, 18 Jun 2024 11:55:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92821b1303c5ddcb3e722c91af39dfee67d938dade7d06501348340be1bafc4b`  
		Last Modified: Tue, 18 Jun 2024 12:06:20 GMT  
		Size: 30.0 MB (30020524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:oracular-20240617`

```console
$ docker pull ubuntu@sha256:1367c15864fc79b5c8ba6be301c83ec2bccf5c1b4a53af71793f740e194598fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:oracular-20240617` - linux; amd64

```console
$ docker pull ubuntu@sha256:2a1e42397521001f21178a06e37ba1024481d3e8b6a754902ac5fb6a0861c7ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29784075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94351b6d67ec74ba3dbc8816e783fd62253ef818a920616c0e6142348af486c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:32 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:34 GMT
ADD file:7de44056586ca78e2d663ff6f13ed78bd93df3759032c25b398020b7f7a508e9 in / 
# Tue, 18 Jun 2024 11:55:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:044e986ad11c8558c1ced47a645123223d7169e0603217f6b5810ae6d5ed8990`  
		Last Modified: Tue, 18 Jun 2024 12:05:48 GMT  
		Size: 29.8 MB (29784075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240617` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:454de8793a5d34b0dee0dbd13719a2c6eeadd7944bacdcace19263cbe9b3a94e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26906015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c89d5967405dc83e44998f274cee92367c1a5535fedf5b28786b266541ed4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:40 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:46 GMT
ADD file:c13178f5cbf3534e02829f373860ffe37af2e84d45812bd7eabc39b4e79bf01a in / 
# Tue, 18 Jun 2024 11:55:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26cb78abf3e6e59cb1ecc37a2ce7bfa44b6eea15ae8bd75ae12a67b744fb8a14`  
		Last Modified: Tue, 18 Jun 2024 12:06:00 GMT  
		Size: 26.9 MB (26906015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240617` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0f58dd64e1e2b1f2c96e2b2cab30402540724a399061b035051534808114144a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28910084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098a556a9a5dea3e4f745912c1182f1a25e8814ed8f855b4221bd99bb15e0d61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:34 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:40 GMT
ADD file:34ce123f3395299e473794d0c46e368375bf7c9630a67258382f114f83a82c40 in / 
# Tue, 18 Jun 2024 11:55:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8fecd43832f92adee10b7b226a92bb3186239d955e0f1d97d8239791a46784fe`  
		Last Modified: Tue, 18 Jun 2024 12:05:54 GMT  
		Size: 28.9 MB (28910084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240617` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ab0729c8fa6a0ab6a3eb07d31438b079e5823107c47b40bffdf8d6c23d5ea542
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34468676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a867e4f4fc9ad515223d70da1936dc4715dfc470d5b12767ef2e5a0bc1cac43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 10:39:06 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:39:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:39:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:39:06 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 10:39:10 GMT
ADD file:3a2687ed020c5070cf555af85025ee8ecf7891a467a2e7122bbeba895861d0b0 in / 
# Tue, 18 Jun 2024 10:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e5aa51133e1c5d213e45194cbadfbfe99c6a335d3391eb4068a9a4f71a4d9c68`  
		Last Modified: Tue, 18 Jun 2024 12:06:07 GMT  
		Size: 34.5 MB (34468676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240617` - linux; s390x

```console
$ docker pull ubuntu@sha256:579f926bf5b5737bb4a6e7a96a26b972ff53efd0e897ca6ad60a5177f646fc23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30020524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acda71050f1c0d987f22287e80bf0f8d8053b3603156d7110c4c8ac85ce1d13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:36 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:39 GMT
ADD file:4bdbaa8c03466d03a76656bbdf683d02b08207350051e5d5d8d46f60ae2ebffd in / 
# Tue, 18 Jun 2024 11:55:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92821b1303c5ddcb3e722c91af39dfee67d938dade7d06501348340be1bafc4b`  
		Last Modified: Tue, 18 Jun 2024 12:06:20 GMT  
		Size: 30.0 MB (30020524 bytes)  
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
