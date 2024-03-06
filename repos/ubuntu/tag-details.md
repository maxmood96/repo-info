<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240216`](#ubuntufocal-20240216)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240227`](#ubuntujammy-20240227)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20240216`](#ubuntumantic-20240216)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240225`](#ubuntunoble-20240225)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:80ef4a44043dec4490506e6cc4289eeda2d106a70148b74b5ae91ee670e9c35d
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
$ docker pull ubuntu@sha256:48c35f3de33487442af224ed4aabac19fd9bfbd91ee90e9471d412706b20ba73
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27514312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cff1c6ff37e0101a08119d0743ba95c7f505d00298f5a169129e4e9086cde9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:edde5e2abc986b867eb41ef92d5d15f3d0bd96ceef11d2bdec1cc8bf32d2fafc
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23621797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5965aa0f973264d9275f2aa1e826a35ce43061e43d6ff57df2e9f687f8c53a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:80753a4d32b0fb1575ed6b69dd721ea5b75d6b104776124b3d3539109a1268e8`  
		Last Modified: Fri, 16 Feb 2024 21:41:05 GMT  
		Size: 23.6 MB (23621797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:4aa61d4985265be6d872cc214016f2f91a77b1c925dab5ce502db2edc4a7e5af
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3048ba0785953b689215053519eb1c34853e2e3af512eed001be59fec1f32e42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:bfa3015908143dd401cc6d0dbd9f0571ff9e087caead46867ce12abac0a4de42
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a17c1701fa251e5b67bec65b30806df72254eaf34f27ae067b98d47162bf24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:38dfc0ab6c0b1b6c56d726c3ed7ccbb809c0f85c5d85e9dbed8fed77007c4ed0`  
		Last Modified: Fri, 16 Feb 2024 21:41:11 GMT  
		Size: 32.1 MB (32076591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec4322e32bcfa82398237d2c6c302aff8888667d80be51ee3c91499e868912f7
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2a45ccd9358494c9e4fa503e98c7c63e1ee22b85f68d2e86965cdf17ef407e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:61d592d9c99b883e7746d2b48b3487d157e1a25c50c85ce08709b8f6c2c55516`  
		Last Modified: Fri, 16 Feb 2024 21:41:17 GMT  
		Size: 26.4 MB (26363167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:77906da86b60585ce12215807090eb327e7386c8fafb5402369e421f44eff17e
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
$ docker pull ubuntu@sha256:aa772c98400ef833586d1d517d3e8de670f7e712bf581ce6053165081773259d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29538961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2b0f26964cf2e80ba3e084d5983dab293fdb87485dc6445f3f7bbfc89d7459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7409efd2c351d36aaca162069e56a19fa2633944215cc478832a72d7eadfaf10
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dea5b6eea26c84e5d7706349bcab9f14b2cd39b98ec31a6c61b523fcaea055`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:abb4a589b6575b27b3632780f584416e354f1d3596a2b98cee1cc8dcd76ebe6e`  
		Last Modified: Tue, 27 Feb 2024 19:00:21 GMT  
		Size: 26.6 MB (26637029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7185d738658e31c96b3ba0f9deaae1df46a5c405dc82025094a51e5e2072212a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7cc08dcdbbb25bd0fe2ddc259b4d794755250f445e6565cb4728be9dc4c0a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:42c4c24813818c3794041522624f4e4def6ad49b900c3ac2762ffc61c25a4461
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34493757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b8145dd8133768e13c4e9f66c96cea5e354218ea5edb1e38dee2b040893774`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ec9849f84ea05dcddad3aae1dad17f2f49b3b950c39945bf0207824781a4dc58`  
		Last Modified: Tue, 27 Feb 2024 19:00:28 GMT  
		Size: 34.5 MB (34493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:c1c8dcac0e924911158b38838474ca79f06b16c281ab11bbac64db7421adf93c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28011097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d262aab8d61754d9a2f504fdaa68760184b93c73b03b11d40e152af4c9ebb9f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:137c4868f69560c0e626198e084a56f05d140f3ac9de35f029d58db50ee2bdd3`  
		Last Modified: Tue, 27 Feb 2024 19:00:35 GMT  
		Size: 28.0 MB (28011097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:5cd569b792a8b7b483d90942381cd7e0b03f0a15520d6e23fb7a1464a25a71b1
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
$ docker pull ubuntu@sha256:50ec5c3a1814f5ef82a564fae94f6b4c5d550bb71614ba6cfe8fadbd8ada9f12
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27231381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee8f4dd2279a19c52eed37256f7a9c67a2d28ff33299207cc8c280844e27e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:062e51aa1fb4497484a7fc4a8af2a195ef9d2085c08cd354c46c8fd5e13b2dc1`  
		Last Modified: Fri, 16 Feb 2024 10:10:01 GMT  
		Size: 27.2 MB (27231381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8079e5e1552317ec1f8c4068e70d5d014e6b2ff9874c5a5678eccd54d9f065f0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24885896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247030744417f06eb6382e948ddfe2f57f8d8e4b1c51df7025f84cf5ee103f78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e3f774185ceccc03a50cbfed313cdc73ed59c0f8fba040dd72a6b22833da29cf`  
		Last Modified: Fri, 16 Feb 2024 10:10:13 GMT  
		Size: 24.9 MB (24885896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a824f88af506abb9b62cf8538c5a46148791426e7bc487b56e8e335464318f01
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26403809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b040c5e70c1ad68e58bb14c713e4785f062a88d3bf194aebcb792256b8c0c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bb583e6d00d7eda6ff4dee98820c0d99b95a26c29db459754e0559b7cc6aca81`  
		Last Modified: Fri, 16 Feb 2024 10:10:07 GMT  
		Size: 26.4 MB (26403809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:0d23b4470c8433fc1d740df2b89314299cc68f39ce2444afd84c69b798287461
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4277f16768863494991088928807feb9f2cdbbf864a3414624319e165c67e554`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cea8b4dc972802b07bb20101aeaab6908636ca6103fb978ab293d5c0b6baf607`  
		Last Modified: Fri, 16 Feb 2024 10:10:20 GMT  
		Size: 31.4 MB (31360599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:d895ad5844f8a08cc3f8f581d4d5259e8d8f5537105c0a625816cf1a43e673c1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27330799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05df7aa76779f5fe17145c195de7e3985551f60a651b837829aed9d8683a292c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58657c921d19932730936612f9e0af9e1499d54e6472b9c0c9bc9854d7096e42`  
		Last Modified: Fri, 16 Feb 2024 10:10:27 GMT  
		Size: 27.3 MB (27330799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:723ad8033f109978f8c7e6421ee684efb624eb5b9251b70c6788fdb2405d050b
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
$ docker pull ubuntu@sha256:69ce9399fe60c5710baee8416b7991183653c3d577afc2b0e3bfe508d7c76142
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29682656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca87e6c45a8ac44c20b05114a68e6c21d0b507c1bf6731dc4c31f832d0757549`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26489f2f1781332c4e802d1dce0cf4978a1b210b92984bd4183dd65a12c163b4`  
		Last Modified: Sun, 25 Feb 2024 04:34:57 GMT  
		Size: 29.7 MB (29682656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0e3ca42b1dbee9ea2803c536d7f1de9d5c468b4bbd76f225002a671a8f38b63c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26868021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb494e330a6fdcbb838a6138ec88025760bd579f714c7ee37e44451acf8819d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43d4081b28c7e5126b5b23344b242f4fa88555eb3158d33599f171c5e3f24376`  
		Last Modified: Sun, 25 Feb 2024 04:35:09 GMT  
		Size: 26.9 MB (26868021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6633ff3b87e40bf09281277f1072458819e915da008095ebdcc76c921a3628a1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28811754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b441975c4aaa1e65a26d9f775a33031eab9282212b774dfc5fd1f49893bcf655`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4299585fd60c199a744f6a4bae61e64df04e0b0ea9343782969dfb58ed706364`  
		Last Modified: Sun, 25 Feb 2024 04:35:03 GMT  
		Size: 28.8 MB (28811754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e216b8a6300fcbaaa6ed713d5dd7f1bad756796727bf89b9d53065eca1e3a11c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34535889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e8c8b15faf9311766f34c7835cd30885647aedbc62b5dc9eb777cf90b6a08`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e2d3a0e37092978e7722d41b840f09348fcf3b4c632d40257031ad2728fbd82`  
		Last Modified: Sun, 25 Feb 2024 04:35:17 GMT  
		Size: 34.5 MB (34535889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:2160a53ecd911097083127476ae5865f365ffa9122eb8e922410e4b706dbc9b0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30006365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a671b74a87efd5ab0005737c0585e2269e6c45b6cab5cb40a246b322b5173`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:126d36364d3a55118896ebf84e37b7bd5b5eafe7f82ecea0588ec54e491cb570`  
		Last Modified: Sun, 25 Feb 2024 04:35:23 GMT  
		Size: 30.0 MB (30006365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:723ad8033f109978f8c7e6421ee684efb624eb5b9251b70c6788fdb2405d050b
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
$ docker pull ubuntu@sha256:69ce9399fe60c5710baee8416b7991183653c3d577afc2b0e3bfe508d7c76142
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29682656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca87e6c45a8ac44c20b05114a68e6c21d0b507c1bf6731dc4c31f832d0757549`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26489f2f1781332c4e802d1dce0cf4978a1b210b92984bd4183dd65a12c163b4`  
		Last Modified: Sun, 25 Feb 2024 04:34:57 GMT  
		Size: 29.7 MB (29682656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0e3ca42b1dbee9ea2803c536d7f1de9d5c468b4bbd76f225002a671a8f38b63c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26868021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb494e330a6fdcbb838a6138ec88025760bd579f714c7ee37e44451acf8819d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43d4081b28c7e5126b5b23344b242f4fa88555eb3158d33599f171c5e3f24376`  
		Last Modified: Sun, 25 Feb 2024 04:35:09 GMT  
		Size: 26.9 MB (26868021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6633ff3b87e40bf09281277f1072458819e915da008095ebdcc76c921a3628a1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28811754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b441975c4aaa1e65a26d9f775a33031eab9282212b774dfc5fd1f49893bcf655`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4299585fd60c199a744f6a4bae61e64df04e0b0ea9343782969dfb58ed706364`  
		Last Modified: Sun, 25 Feb 2024 04:35:03 GMT  
		Size: 28.8 MB (28811754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e216b8a6300fcbaaa6ed713d5dd7f1bad756796727bf89b9d53065eca1e3a11c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34535889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e8c8b15faf9311766f34c7835cd30885647aedbc62b5dc9eb777cf90b6a08`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e2d3a0e37092978e7722d41b840f09348fcf3b4c632d40257031ad2728fbd82`  
		Last Modified: Sun, 25 Feb 2024 04:35:17 GMT  
		Size: 34.5 MB (34535889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:2160a53ecd911097083127476ae5865f365ffa9122eb8e922410e4b706dbc9b0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30006365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a671b74a87efd5ab0005737c0585e2269e6c45b6cab5cb40a246b322b5173`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:126d36364d3a55118896ebf84e37b7bd5b5eafe7f82ecea0588ec54e491cb570`  
		Last Modified: Sun, 25 Feb 2024 04:35:23 GMT  
		Size: 30.0 MB (30006365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:80ef4a44043dec4490506e6cc4289eeda2d106a70148b74b5ae91ee670e9c35d
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
$ docker pull ubuntu@sha256:48c35f3de33487442af224ed4aabac19fd9bfbd91ee90e9471d412706b20ba73
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27514312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cff1c6ff37e0101a08119d0743ba95c7f505d00298f5a169129e4e9086cde9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:edde5e2abc986b867eb41ef92d5d15f3d0bd96ceef11d2bdec1cc8bf32d2fafc
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23621797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5965aa0f973264d9275f2aa1e826a35ce43061e43d6ff57df2e9f687f8c53a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:80753a4d32b0fb1575ed6b69dd721ea5b75d6b104776124b3d3539109a1268e8`  
		Last Modified: Fri, 16 Feb 2024 21:41:05 GMT  
		Size: 23.6 MB (23621797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:4aa61d4985265be6d872cc214016f2f91a77b1c925dab5ce502db2edc4a7e5af
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3048ba0785953b689215053519eb1c34853e2e3af512eed001be59fec1f32e42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:bfa3015908143dd401cc6d0dbd9f0571ff9e087caead46867ce12abac0a4de42
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a17c1701fa251e5b67bec65b30806df72254eaf34f27ae067b98d47162bf24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:38dfc0ab6c0b1b6c56d726c3ed7ccbb809c0f85c5d85e9dbed8fed77007c4ed0`  
		Last Modified: Fri, 16 Feb 2024 21:41:11 GMT  
		Size: 32.1 MB (32076591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec4322e32bcfa82398237d2c6c302aff8888667d80be51ee3c91499e868912f7
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2a45ccd9358494c9e4fa503e98c7c63e1ee22b85f68d2e86965cdf17ef407e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:61d592d9c99b883e7746d2b48b3487d157e1a25c50c85ce08709b8f6c2c55516`  
		Last Modified: Fri, 16 Feb 2024 21:41:17 GMT  
		Size: 26.4 MB (26363167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240216`

```console
$ docker pull ubuntu@sha256:80ef4a44043dec4490506e6cc4289eeda2d106a70148b74b5ae91ee670e9c35d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20240216` - linux; amd64

```console
$ docker pull ubuntu@sha256:48c35f3de33487442af224ed4aabac19fd9bfbd91ee90e9471d412706b20ba73
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27514312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cff1c6ff37e0101a08119d0743ba95c7f505d00298f5a169129e4e9086cde9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240216` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:edde5e2abc986b867eb41ef92d5d15f3d0bd96ceef11d2bdec1cc8bf32d2fafc
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23621797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5965aa0f973264d9275f2aa1e826a35ce43061e43d6ff57df2e9f687f8c53a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:80753a4d32b0fb1575ed6b69dd721ea5b75d6b104776124b3d3539109a1268e8`  
		Last Modified: Fri, 16 Feb 2024 21:41:05 GMT  
		Size: 23.6 MB (23621797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240216` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:4aa61d4985265be6d872cc214016f2f91a77b1c925dab5ce502db2edc4a7e5af
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3048ba0785953b689215053519eb1c34853e2e3af512eed001be59fec1f32e42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240216` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:bfa3015908143dd401cc6d0dbd9f0571ff9e087caead46867ce12abac0a4de42
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a17c1701fa251e5b67bec65b30806df72254eaf34f27ae067b98d47162bf24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:38dfc0ab6c0b1b6c56d726c3ed7ccbb809c0f85c5d85e9dbed8fed77007c4ed0`  
		Last Modified: Fri, 16 Feb 2024 21:41:11 GMT  
		Size: 32.1 MB (32076591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240216` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec4322e32bcfa82398237d2c6c302aff8888667d80be51ee3c91499e868912f7
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2a45ccd9358494c9e4fa503e98c7c63e1ee22b85f68d2e86965cdf17ef407e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:61d592d9c99b883e7746d2b48b3487d157e1a25c50c85ce08709b8f6c2c55516`  
		Last Modified: Fri, 16 Feb 2024 21:41:17 GMT  
		Size: 26.4 MB (26363167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:77906da86b60585ce12215807090eb327e7386c8fafb5402369e421f44eff17e
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
$ docker pull ubuntu@sha256:aa772c98400ef833586d1d517d3e8de670f7e712bf581ce6053165081773259d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29538961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2b0f26964cf2e80ba3e084d5983dab293fdb87485dc6445f3f7bbfc89d7459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7409efd2c351d36aaca162069e56a19fa2633944215cc478832a72d7eadfaf10
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dea5b6eea26c84e5d7706349bcab9f14b2cd39b98ec31a6c61b523fcaea055`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:abb4a589b6575b27b3632780f584416e354f1d3596a2b98cee1cc8dcd76ebe6e`  
		Last Modified: Tue, 27 Feb 2024 19:00:21 GMT  
		Size: 26.6 MB (26637029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7185d738658e31c96b3ba0f9deaae1df46a5c405dc82025094a51e5e2072212a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7cc08dcdbbb25bd0fe2ddc259b4d794755250f445e6565cb4728be9dc4c0a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:42c4c24813818c3794041522624f4e4def6ad49b900c3ac2762ffc61c25a4461
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34493757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b8145dd8133768e13c4e9f66c96cea5e354218ea5edb1e38dee2b040893774`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ec9849f84ea05dcddad3aae1dad17f2f49b3b950c39945bf0207824781a4dc58`  
		Last Modified: Tue, 27 Feb 2024 19:00:28 GMT  
		Size: 34.5 MB (34493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:c1c8dcac0e924911158b38838474ca79f06b16c281ab11bbac64db7421adf93c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28011097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d262aab8d61754d9a2f504fdaa68760184b93c73b03b11d40e152af4c9ebb9f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:137c4868f69560c0e626198e084a56f05d140f3ac9de35f029d58db50ee2bdd3`  
		Last Modified: Tue, 27 Feb 2024 19:00:35 GMT  
		Size: 28.0 MB (28011097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240227`

```console
$ docker pull ubuntu@sha256:77906da86b60585ce12215807090eb327e7386c8fafb5402369e421f44eff17e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20240227` - linux; amd64

```console
$ docker pull ubuntu@sha256:aa772c98400ef833586d1d517d3e8de670f7e712bf581ce6053165081773259d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29538961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2b0f26964cf2e80ba3e084d5983dab293fdb87485dc6445f3f7bbfc89d7459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240227` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7409efd2c351d36aaca162069e56a19fa2633944215cc478832a72d7eadfaf10
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dea5b6eea26c84e5d7706349bcab9f14b2cd39b98ec31a6c61b523fcaea055`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:abb4a589b6575b27b3632780f584416e354f1d3596a2b98cee1cc8dcd76ebe6e`  
		Last Modified: Tue, 27 Feb 2024 19:00:21 GMT  
		Size: 26.6 MB (26637029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240227` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7185d738658e31c96b3ba0f9deaae1df46a5c405dc82025094a51e5e2072212a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7cc08dcdbbb25bd0fe2ddc259b4d794755250f445e6565cb4728be9dc4c0a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240227` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:42c4c24813818c3794041522624f4e4def6ad49b900c3ac2762ffc61c25a4461
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34493757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b8145dd8133768e13c4e9f66c96cea5e354218ea5edb1e38dee2b040893774`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ec9849f84ea05dcddad3aae1dad17f2f49b3b950c39945bf0207824781a4dc58`  
		Last Modified: Tue, 27 Feb 2024 19:00:28 GMT  
		Size: 34.5 MB (34493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240227` - linux; s390x

```console
$ docker pull ubuntu@sha256:c1c8dcac0e924911158b38838474ca79f06b16c281ab11bbac64db7421adf93c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28011097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d262aab8d61754d9a2f504fdaa68760184b93c73b03b11d40e152af4c9ebb9f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:137c4868f69560c0e626198e084a56f05d140f3ac9de35f029d58db50ee2bdd3`  
		Last Modified: Tue, 27 Feb 2024 19:00:35 GMT  
		Size: 28.0 MB (28011097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:77906da86b60585ce12215807090eb327e7386c8fafb5402369e421f44eff17e
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
$ docker pull ubuntu@sha256:aa772c98400ef833586d1d517d3e8de670f7e712bf581ce6053165081773259d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29538961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2b0f26964cf2e80ba3e084d5983dab293fdb87485dc6445f3f7bbfc89d7459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7409efd2c351d36aaca162069e56a19fa2633944215cc478832a72d7eadfaf10
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dea5b6eea26c84e5d7706349bcab9f14b2cd39b98ec31a6c61b523fcaea055`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:abb4a589b6575b27b3632780f584416e354f1d3596a2b98cee1cc8dcd76ebe6e`  
		Last Modified: Tue, 27 Feb 2024 19:00:21 GMT  
		Size: 26.6 MB (26637029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7185d738658e31c96b3ba0f9deaae1df46a5c405dc82025094a51e5e2072212a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7cc08dcdbbb25bd0fe2ddc259b4d794755250f445e6565cb4728be9dc4c0a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:42c4c24813818c3794041522624f4e4def6ad49b900c3ac2762ffc61c25a4461
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34493757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b8145dd8133768e13c4e9f66c96cea5e354218ea5edb1e38dee2b040893774`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ec9849f84ea05dcddad3aae1dad17f2f49b3b950c39945bf0207824781a4dc58`  
		Last Modified: Tue, 27 Feb 2024 19:00:28 GMT  
		Size: 34.5 MB (34493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:c1c8dcac0e924911158b38838474ca79f06b16c281ab11bbac64db7421adf93c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28011097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d262aab8d61754d9a2f504fdaa68760184b93c73b03b11d40e152af4c9ebb9f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:137c4868f69560c0e626198e084a56f05d140f3ac9de35f029d58db50ee2bdd3`  
		Last Modified: Tue, 27 Feb 2024 19:00:35 GMT  
		Size: 28.0 MB (28011097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:5cd569b792a8b7b483d90942381cd7e0b03f0a15520d6e23fb7a1464a25a71b1
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
$ docker pull ubuntu@sha256:50ec5c3a1814f5ef82a564fae94f6b4c5d550bb71614ba6cfe8fadbd8ada9f12
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27231381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee8f4dd2279a19c52eed37256f7a9c67a2d28ff33299207cc8c280844e27e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:062e51aa1fb4497484a7fc4a8af2a195ef9d2085c08cd354c46c8fd5e13b2dc1`  
		Last Modified: Fri, 16 Feb 2024 10:10:01 GMT  
		Size: 27.2 MB (27231381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8079e5e1552317ec1f8c4068e70d5d014e6b2ff9874c5a5678eccd54d9f065f0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24885896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247030744417f06eb6382e948ddfe2f57f8d8e4b1c51df7025f84cf5ee103f78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e3f774185ceccc03a50cbfed313cdc73ed59c0f8fba040dd72a6b22833da29cf`  
		Last Modified: Fri, 16 Feb 2024 10:10:13 GMT  
		Size: 24.9 MB (24885896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a824f88af506abb9b62cf8538c5a46148791426e7bc487b56e8e335464318f01
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26403809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b040c5e70c1ad68e58bb14c713e4785f062a88d3bf194aebcb792256b8c0c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bb583e6d00d7eda6ff4dee98820c0d99b95a26c29db459754e0559b7cc6aca81`  
		Last Modified: Fri, 16 Feb 2024 10:10:07 GMT  
		Size: 26.4 MB (26403809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:0d23b4470c8433fc1d740df2b89314299cc68f39ce2444afd84c69b798287461
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4277f16768863494991088928807feb9f2cdbbf864a3414624319e165c67e554`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cea8b4dc972802b07bb20101aeaab6908636ca6103fb978ab293d5c0b6baf607`  
		Last Modified: Fri, 16 Feb 2024 10:10:20 GMT  
		Size: 31.4 MB (31360599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:d895ad5844f8a08cc3f8f581d4d5259e8d8f5537105c0a625816cf1a43e673c1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27330799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05df7aa76779f5fe17145c195de7e3985551f60a651b837829aed9d8683a292c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58657c921d19932730936612f9e0af9e1499d54e6472b9c0c9bc9854d7096e42`  
		Last Modified: Fri, 16 Feb 2024 10:10:27 GMT  
		Size: 27.3 MB (27330799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20240216`

```console
$ docker pull ubuntu@sha256:5cd569b792a8b7b483d90942381cd7e0b03f0a15520d6e23fb7a1464a25a71b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20240216` - linux; amd64

```console
$ docker pull ubuntu@sha256:50ec5c3a1814f5ef82a564fae94f6b4c5d550bb71614ba6cfe8fadbd8ada9f12
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27231381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee8f4dd2279a19c52eed37256f7a9c67a2d28ff33299207cc8c280844e27e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:062e51aa1fb4497484a7fc4a8af2a195ef9d2085c08cd354c46c8fd5e13b2dc1`  
		Last Modified: Fri, 16 Feb 2024 10:10:01 GMT  
		Size: 27.2 MB (27231381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240216` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8079e5e1552317ec1f8c4068e70d5d014e6b2ff9874c5a5678eccd54d9f065f0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24885896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247030744417f06eb6382e948ddfe2f57f8d8e4b1c51df7025f84cf5ee103f78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e3f774185ceccc03a50cbfed313cdc73ed59c0f8fba040dd72a6b22833da29cf`  
		Last Modified: Fri, 16 Feb 2024 10:10:13 GMT  
		Size: 24.9 MB (24885896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240216` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a824f88af506abb9b62cf8538c5a46148791426e7bc487b56e8e335464318f01
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26403809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b040c5e70c1ad68e58bb14c713e4785f062a88d3bf194aebcb792256b8c0c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bb583e6d00d7eda6ff4dee98820c0d99b95a26c29db459754e0559b7cc6aca81`  
		Last Modified: Fri, 16 Feb 2024 10:10:07 GMT  
		Size: 26.4 MB (26403809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240216` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:0d23b4470c8433fc1d740df2b89314299cc68f39ce2444afd84c69b798287461
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4277f16768863494991088928807feb9f2cdbbf864a3414624319e165c67e554`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cea8b4dc972802b07bb20101aeaab6908636ca6103fb978ab293d5c0b6baf607`  
		Last Modified: Fri, 16 Feb 2024 10:10:20 GMT  
		Size: 31.4 MB (31360599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240216` - linux; s390x

```console
$ docker pull ubuntu@sha256:d895ad5844f8a08cc3f8f581d4d5259e8d8f5537105c0a625816cf1a43e673c1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27330799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05df7aa76779f5fe17145c195de7e3985551f60a651b837829aed9d8683a292c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58657c921d19932730936612f9e0af9e1499d54e6472b9c0c9bc9854d7096e42`  
		Last Modified: Fri, 16 Feb 2024 10:10:27 GMT  
		Size: 27.3 MB (27330799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:723ad8033f109978f8c7e6421ee684efb624eb5b9251b70c6788fdb2405d050b
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
$ docker pull ubuntu@sha256:69ce9399fe60c5710baee8416b7991183653c3d577afc2b0e3bfe508d7c76142
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29682656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca87e6c45a8ac44c20b05114a68e6c21d0b507c1bf6731dc4c31f832d0757549`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26489f2f1781332c4e802d1dce0cf4978a1b210b92984bd4183dd65a12c163b4`  
		Last Modified: Sun, 25 Feb 2024 04:34:57 GMT  
		Size: 29.7 MB (29682656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0e3ca42b1dbee9ea2803c536d7f1de9d5c468b4bbd76f225002a671a8f38b63c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26868021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb494e330a6fdcbb838a6138ec88025760bd579f714c7ee37e44451acf8819d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43d4081b28c7e5126b5b23344b242f4fa88555eb3158d33599f171c5e3f24376`  
		Last Modified: Sun, 25 Feb 2024 04:35:09 GMT  
		Size: 26.9 MB (26868021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6633ff3b87e40bf09281277f1072458819e915da008095ebdcc76c921a3628a1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28811754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b441975c4aaa1e65a26d9f775a33031eab9282212b774dfc5fd1f49893bcf655`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4299585fd60c199a744f6a4bae61e64df04e0b0ea9343782969dfb58ed706364`  
		Last Modified: Sun, 25 Feb 2024 04:35:03 GMT  
		Size: 28.8 MB (28811754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e216b8a6300fcbaaa6ed713d5dd7f1bad756796727bf89b9d53065eca1e3a11c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34535889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e8c8b15faf9311766f34c7835cd30885647aedbc62b5dc9eb777cf90b6a08`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e2d3a0e37092978e7722d41b840f09348fcf3b4c632d40257031ad2728fbd82`  
		Last Modified: Sun, 25 Feb 2024 04:35:17 GMT  
		Size: 34.5 MB (34535889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:2160a53ecd911097083127476ae5865f365ffa9122eb8e922410e4b706dbc9b0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30006365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a671b74a87efd5ab0005737c0585e2269e6c45b6cab5cb40a246b322b5173`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:126d36364d3a55118896ebf84e37b7bd5b5eafe7f82ecea0588ec54e491cb570`  
		Last Modified: Sun, 25 Feb 2024 04:35:23 GMT  
		Size: 30.0 MB (30006365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240225`

```console
$ docker pull ubuntu@sha256:723ad8033f109978f8c7e6421ee684efb624eb5b9251b70c6788fdb2405d050b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble-20240225` - linux; amd64

```console
$ docker pull ubuntu@sha256:69ce9399fe60c5710baee8416b7991183653c3d577afc2b0e3bfe508d7c76142
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29682656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca87e6c45a8ac44c20b05114a68e6c21d0b507c1bf6731dc4c31f832d0757549`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26489f2f1781332c4e802d1dce0cf4978a1b210b92984bd4183dd65a12c163b4`  
		Last Modified: Sun, 25 Feb 2024 04:34:57 GMT  
		Size: 29.7 MB (29682656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240225` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0e3ca42b1dbee9ea2803c536d7f1de9d5c468b4bbd76f225002a671a8f38b63c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26868021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb494e330a6fdcbb838a6138ec88025760bd579f714c7ee37e44451acf8819d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43d4081b28c7e5126b5b23344b242f4fa88555eb3158d33599f171c5e3f24376`  
		Last Modified: Sun, 25 Feb 2024 04:35:09 GMT  
		Size: 26.9 MB (26868021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240225` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6633ff3b87e40bf09281277f1072458819e915da008095ebdcc76c921a3628a1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28811754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b441975c4aaa1e65a26d9f775a33031eab9282212b774dfc5fd1f49893bcf655`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4299585fd60c199a744f6a4bae61e64df04e0b0ea9343782969dfb58ed706364`  
		Last Modified: Sun, 25 Feb 2024 04:35:03 GMT  
		Size: 28.8 MB (28811754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240225` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e216b8a6300fcbaaa6ed713d5dd7f1bad756796727bf89b9d53065eca1e3a11c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34535889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e8c8b15faf9311766f34c7835cd30885647aedbc62b5dc9eb777cf90b6a08`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e2d3a0e37092978e7722d41b840f09348fcf3b4c632d40257031ad2728fbd82`  
		Last Modified: Sun, 25 Feb 2024 04:35:17 GMT  
		Size: 34.5 MB (34535889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240225` - linux; s390x

```console
$ docker pull ubuntu@sha256:2160a53ecd911097083127476ae5865f365ffa9122eb8e922410e4b706dbc9b0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30006365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a671b74a87efd5ab0005737c0585e2269e6c45b6cab5cb40a246b322b5173`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:126d36364d3a55118896ebf84e37b7bd5b5eafe7f82ecea0588ec54e491cb570`  
		Last Modified: Sun, 25 Feb 2024 04:35:23 GMT  
		Size: 30.0 MB (30006365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:5cd569b792a8b7b483d90942381cd7e0b03f0a15520d6e23fb7a1464a25a71b1
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
$ docker pull ubuntu@sha256:50ec5c3a1814f5ef82a564fae94f6b4c5d550bb71614ba6cfe8fadbd8ada9f12
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27231381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee8f4dd2279a19c52eed37256f7a9c67a2d28ff33299207cc8c280844e27e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:062e51aa1fb4497484a7fc4a8af2a195ef9d2085c08cd354c46c8fd5e13b2dc1`  
		Last Modified: Fri, 16 Feb 2024 10:10:01 GMT  
		Size: 27.2 MB (27231381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8079e5e1552317ec1f8c4068e70d5d014e6b2ff9874c5a5678eccd54d9f065f0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24885896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247030744417f06eb6382e948ddfe2f57f8d8e4b1c51df7025f84cf5ee103f78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e3f774185ceccc03a50cbfed313cdc73ed59c0f8fba040dd72a6b22833da29cf`  
		Last Modified: Fri, 16 Feb 2024 10:10:13 GMT  
		Size: 24.9 MB (24885896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a824f88af506abb9b62cf8538c5a46148791426e7bc487b56e8e335464318f01
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26403809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b040c5e70c1ad68e58bb14c713e4785f062a88d3bf194aebcb792256b8c0c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bb583e6d00d7eda6ff4dee98820c0d99b95a26c29db459754e0559b7cc6aca81`  
		Last Modified: Fri, 16 Feb 2024 10:10:07 GMT  
		Size: 26.4 MB (26403809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:0d23b4470c8433fc1d740df2b89314299cc68f39ce2444afd84c69b798287461
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4277f16768863494991088928807feb9f2cdbbf864a3414624319e165c67e554`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cea8b4dc972802b07bb20101aeaab6908636ca6103fb978ab293d5c0b6baf607`  
		Last Modified: Fri, 16 Feb 2024 10:10:20 GMT  
		Size: 31.4 MB (31360599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:d895ad5844f8a08cc3f8f581d4d5259e8d8f5537105c0a625816cf1a43e673c1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27330799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05df7aa76779f5fe17145c195de7e3985551f60a651b837829aed9d8683a292c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58657c921d19932730936612f9e0af9e1499d54e6472b9c0c9bc9854d7096e42`  
		Last Modified: Fri, 16 Feb 2024 10:10:27 GMT  
		Size: 27.3 MB (27330799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
