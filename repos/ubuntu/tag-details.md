<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240410`](#ubuntufocal-20240410)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240405`](#ubuntujammy-20240405)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20240405`](#ubuntumantic-20240405)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240407.1`](#ubuntunoble-202404071)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:c97a46bb9b30a4a957464fd07c55f1612c800513bdbc7ff798ec08a6bd94b5ef
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
$ docker pull ubuntu@sha256:bd8a5c42887492c47adc873b855753158392742c0d9155c6bc2a0c5d0e3dcd82
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13b0a84dab9cf0b088f39766fab7ba58ba42d1414ccf0ead6203f371923788`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:78102c38ae65613b2ee783b6958bab73ce162f03487b33a21174bee44d9fb37a`  
		Last Modified: Wed, 10 Apr 2024 19:19:31 GMT  
		Size: 23.6 MB (23622898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d40777b9a5329d3611f7bc40738b4cd459c8b1508fa8cc7c1555674c40671598
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcc83a51b0096c961e9431235462f6402e148368c77d99392a51a0da5b9b8b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
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
$ docker pull ubuntu@sha256:7faa8d7f57e4188578989d11813405b5ae04bc1ae3340758bcc0b8f82a04696a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26366699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707f53d2a103ac02d37a169339f3ed9df99e027f994f7d0335a5ad237067da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:51:34 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:51:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:51:38 GMT
ADD file:c91b061ad49bce1f6e2860bfe87ed2e94cc280b915289f041d2dd5ce3ef385ad in / 
# Wed, 10 Apr 2024 18:51:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9c9043abb8ba47bd083fee5b16d1e0d6dbb7f1455978a8812b11443832ed103`  
		Last Modified: Wed, 10 Apr 2024 19:19:43 GMT  
		Size: 26.4 MB (26366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:355096553182601ccf2fa8ba88af65b5afa08492e5598fe575c36a9e56f3a133
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
$ docker pull ubuntu@sha256:4eb00f9a877cbabfc91d271a91855278df10f2c1bf80fd56cf210c14fc1f5618
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27715f1115e575122d6207d7d6303b3866f01feda96fdee851618a997ebfe8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b693c0578bb86a6111c6b9770eb9fd6826cee6d2825b5869e3aa66e53454166a`  
		Last Modified: Wed, 10 Apr 2024 19:21:01 GMT  
		Size: 26.6 MB (26637579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c427cc251a507a2459eacd770fe2cd7e451f883b077e09b2d27fa6f129b29d81
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27359551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbcc2701b935fa13b53ee525549d83c27c3560055c578768f1f4d4f1b8bde32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
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
$ docker pull ubuntu@sha256:c194ef08b0f8dadd78c9932865553ec3e045e20b07daba9364fd98a7c2de19fe
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd3ff2b0480cdac7c482efce325c5612a005e4a743f55822537548a8dcfefc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6e1eba39e4ebf768879e23d5cbf0eb1ad6db055027ddec35427160ce576c3d4`  
		Last Modified: Wed, 10 Apr 2024 19:21:13 GMT  
		Size: 28.0 MB (28000125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:de75a9d421d24c1e335a0b1f8083be838c4652da43eb970348ce907f827236b7
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
$ docker pull ubuntu@sha256:d2ef4d29f07d2e34e02bd3edbecd7e97c066a5ac1eddaf726d4dab7b4fd30abd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24887415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6f00029030e4f1fd73079a98f46caac7940db908032c0e53a2dd347ef6fa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a032cb47dd8d01b6383603fb581fd99c856b139e1a013415d969e9421b6803bc`  
		Last Modified: Fri, 12 Apr 2024 16:00:11 GMT  
		Size: 24.9 MB (24887415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1e4c25185533d7bed7864744d2a5b2c43bf1ac7a7f6427267c72828712e4e16a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be742dd48b8ce1c5254b2f75a0f28a5ad54d5cdffe7f198217d9f11618a8f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:942a35531af124aa3c3906d47e8dd6472cec1bfa9ec398abfea155f72c64cc96`  
		Last Modified: Fri, 12 Apr 2024 16:00:05 GMT  
		Size: 26.4 MB (26413454 bytes)  
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
$ docker pull ubuntu@sha256:fb8daccea84b4657e01ec61e5a1d9dbb75739c8096a2580f9ae1e379846feb54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f300c99459926efcebd5cacdab52ee0900534912b1c75db2556cfec826f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2867589a33d86d4239850bd34e12ff3064467a71264788d2dd5d807347b0f1c7`  
		Last Modified: Fri, 12 Apr 2024 16:00:25 GMT  
		Size: 27.3 MB (27331928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:f2e70beb6ac047e6424a1ee723777f63e4b9e636979e8e61609e31aa1fee5d10
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

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b61c7c7b34921e6805388eb4cd2bd7adb40f842af583c7af8eb28d3c50e6ea97
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27980097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa4940cd722b5042f615f16a268ba712e96f0be896c7dd0cf9310c545a5c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c7ec942a10b2818754e030a717ceb80881eef105a2efc304a3afeb2421e78c`  
		Last Modified: Sun, 07 Apr 2024 17:19:11 GMT  
		Size: 28.0 MB (27980097 bytes)  
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
$ docker pull ubuntu@sha256:63c1538627e447932daae84283e194b14c6323c16a29d9bdbe071e8744c5f0b4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f38b99e0ca2a6f55155893071f008bb5b14f2d2afb0a48ded1f22e085ccfcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf319107486d1a8ff3845cc8abca0de71f7437518fe348fce75fb7db345a555`  
		Last Modified: Sun, 07 Apr 2024 17:19:30 GMT  
		Size: 29.1 MB (29113387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:f2e70beb6ac047e6424a1ee723777f63e4b9e636979e8e61609e31aa1fee5d10
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
$ docker pull ubuntu@sha256:b61c7c7b34921e6805388eb4cd2bd7adb40f842af583c7af8eb28d3c50e6ea97
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27980097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa4940cd722b5042f615f16a268ba712e96f0be896c7dd0cf9310c545a5c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c7ec942a10b2818754e030a717ceb80881eef105a2efc304a3afeb2421e78c`  
		Last Modified: Sun, 07 Apr 2024 17:19:11 GMT  
		Size: 28.0 MB (27980097 bytes)  
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
$ docker pull ubuntu@sha256:63c1538627e447932daae84283e194b14c6323c16a29d9bdbe071e8744c5f0b4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f38b99e0ca2a6f55155893071f008bb5b14f2d2afb0a48ded1f22e085ccfcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf319107486d1a8ff3845cc8abca0de71f7437518fe348fce75fb7db345a555`  
		Last Modified: Sun, 07 Apr 2024 17:19:30 GMT  
		Size: 29.1 MB (29113387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:c97a46bb9b30a4a957464fd07c55f1612c800513bdbc7ff798ec08a6bd94b5ef
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
$ docker pull ubuntu@sha256:bd8a5c42887492c47adc873b855753158392742c0d9155c6bc2a0c5d0e3dcd82
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13b0a84dab9cf0b088f39766fab7ba58ba42d1414ccf0ead6203f371923788`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:78102c38ae65613b2ee783b6958bab73ce162f03487b33a21174bee44d9fb37a`  
		Last Modified: Wed, 10 Apr 2024 19:19:31 GMT  
		Size: 23.6 MB (23622898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d40777b9a5329d3611f7bc40738b4cd459c8b1508fa8cc7c1555674c40671598
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcc83a51b0096c961e9431235462f6402e148368c77d99392a51a0da5b9b8b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
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
$ docker pull ubuntu@sha256:7faa8d7f57e4188578989d11813405b5ae04bc1ae3340758bcc0b8f82a04696a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26366699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707f53d2a103ac02d37a169339f3ed9df99e027f994f7d0335a5ad237067da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:51:34 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:51:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:51:38 GMT
ADD file:c91b061ad49bce1f6e2860bfe87ed2e94cc280b915289f041d2dd5ce3ef385ad in / 
# Wed, 10 Apr 2024 18:51:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9c9043abb8ba47bd083fee5b16d1e0d6dbb7f1455978a8812b11443832ed103`  
		Last Modified: Wed, 10 Apr 2024 19:19:43 GMT  
		Size: 26.4 MB (26366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240410`

```console
$ docker pull ubuntu@sha256:f8fd951925e97d6554542c9bf2730b754314d73d5b1423c7b56817cea89da8c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `ubuntu:focal-20240410` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bd8a5c42887492c47adc873b855753158392742c0d9155c6bc2a0c5d0e3dcd82
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13b0a84dab9cf0b088f39766fab7ba58ba42d1414ccf0ead6203f371923788`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:78102c38ae65613b2ee783b6958bab73ce162f03487b33a21174bee44d9fb37a`  
		Last Modified: Wed, 10 Apr 2024 19:19:31 GMT  
		Size: 23.6 MB (23622898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240410` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d40777b9a5329d3611f7bc40738b4cd459c8b1508fa8cc7c1555674c40671598
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcc83a51b0096c961e9431235462f6402e148368c77d99392a51a0da5b9b8b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240410` - linux; s390x

```console
$ docker pull ubuntu@sha256:7faa8d7f57e4188578989d11813405b5ae04bc1ae3340758bcc0b8f82a04696a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26366699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707f53d2a103ac02d37a169339f3ed9df99e027f994f7d0335a5ad237067da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:51:34 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:51:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:51:38 GMT
ADD file:c91b061ad49bce1f6e2860bfe87ed2e94cc280b915289f041d2dd5ce3ef385ad in / 
# Wed, 10 Apr 2024 18:51:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9c9043abb8ba47bd083fee5b16d1e0d6dbb7f1455978a8812b11443832ed103`  
		Last Modified: Wed, 10 Apr 2024 19:19:43 GMT  
		Size: 26.4 MB (26366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:355096553182601ccf2fa8ba88af65b5afa08492e5598fe575c36a9e56f3a133
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
$ docker pull ubuntu@sha256:4eb00f9a877cbabfc91d271a91855278df10f2c1bf80fd56cf210c14fc1f5618
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27715f1115e575122d6207d7d6303b3866f01feda96fdee851618a997ebfe8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b693c0578bb86a6111c6b9770eb9fd6826cee6d2825b5869e3aa66e53454166a`  
		Last Modified: Wed, 10 Apr 2024 19:21:01 GMT  
		Size: 26.6 MB (26637579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c427cc251a507a2459eacd770fe2cd7e451f883b077e09b2d27fa6f129b29d81
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27359551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbcc2701b935fa13b53ee525549d83c27c3560055c578768f1f4d4f1b8bde32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
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
$ docker pull ubuntu@sha256:c194ef08b0f8dadd78c9932865553ec3e045e20b07daba9364fd98a7c2de19fe
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd3ff2b0480cdac7c482efce325c5612a005e4a743f55822537548a8dcfefc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6e1eba39e4ebf768879e23d5cbf0eb1ad6db055027ddec35427160ce576c3d4`  
		Last Modified: Wed, 10 Apr 2024 19:21:13 GMT  
		Size: 28.0 MB (28000125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240405`

```console
$ docker pull ubuntu@sha256:f1d0e3ca11ed98576136845517142d11890fe941b450716fbb2ae19c37102bd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `ubuntu:jammy-20240405` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4eb00f9a877cbabfc91d271a91855278df10f2c1bf80fd56cf210c14fc1f5618
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27715f1115e575122d6207d7d6303b3866f01feda96fdee851618a997ebfe8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b693c0578bb86a6111c6b9770eb9fd6826cee6d2825b5869e3aa66e53454166a`  
		Last Modified: Wed, 10 Apr 2024 19:21:01 GMT  
		Size: 26.6 MB (26637579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240405` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c427cc251a507a2459eacd770fe2cd7e451f883b077e09b2d27fa6f129b29d81
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27359551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbcc2701b935fa13b53ee525549d83c27c3560055c578768f1f4d4f1b8bde32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240405` - linux; s390x

```console
$ docker pull ubuntu@sha256:c194ef08b0f8dadd78c9932865553ec3e045e20b07daba9364fd98a7c2de19fe
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd3ff2b0480cdac7c482efce325c5612a005e4a743f55822537548a8dcfefc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6e1eba39e4ebf768879e23d5cbf0eb1ad6db055027ddec35427160ce576c3d4`  
		Last Modified: Wed, 10 Apr 2024 19:21:13 GMT  
		Size: 28.0 MB (28000125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:355096553182601ccf2fa8ba88af65b5afa08492e5598fe575c36a9e56f3a133
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
$ docker pull ubuntu@sha256:4eb00f9a877cbabfc91d271a91855278df10f2c1bf80fd56cf210c14fc1f5618
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27715f1115e575122d6207d7d6303b3866f01feda96fdee851618a997ebfe8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b693c0578bb86a6111c6b9770eb9fd6826cee6d2825b5869e3aa66e53454166a`  
		Last Modified: Wed, 10 Apr 2024 19:21:01 GMT  
		Size: 26.6 MB (26637579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c427cc251a507a2459eacd770fe2cd7e451f883b077e09b2d27fa6f129b29d81
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27359551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbcc2701b935fa13b53ee525549d83c27c3560055c578768f1f4d4f1b8bde32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
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
$ docker pull ubuntu@sha256:c194ef08b0f8dadd78c9932865553ec3e045e20b07daba9364fd98a7c2de19fe
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd3ff2b0480cdac7c482efce325c5612a005e4a743f55822537548a8dcfefc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6e1eba39e4ebf768879e23d5cbf0eb1ad6db055027ddec35427160ce576c3d4`  
		Last Modified: Wed, 10 Apr 2024 19:21:13 GMT  
		Size: 28.0 MB (28000125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:de75a9d421d24c1e335a0b1f8083be838c4652da43eb970348ce907f827236b7
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
$ docker pull ubuntu@sha256:d2ef4d29f07d2e34e02bd3edbecd7e97c066a5ac1eddaf726d4dab7b4fd30abd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24887415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6f00029030e4f1fd73079a98f46caac7940db908032c0e53a2dd347ef6fa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a032cb47dd8d01b6383603fb581fd99c856b139e1a013415d969e9421b6803bc`  
		Last Modified: Fri, 12 Apr 2024 16:00:11 GMT  
		Size: 24.9 MB (24887415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1e4c25185533d7bed7864744d2a5b2c43bf1ac7a7f6427267c72828712e4e16a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be742dd48b8ce1c5254b2f75a0f28a5ad54d5cdffe7f198217d9f11618a8f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:942a35531af124aa3c3906d47e8dd6472cec1bfa9ec398abfea155f72c64cc96`  
		Last Modified: Fri, 12 Apr 2024 16:00:05 GMT  
		Size: 26.4 MB (26413454 bytes)  
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
$ docker pull ubuntu@sha256:fb8daccea84b4657e01ec61e5a1d9dbb75739c8096a2580f9ae1e379846feb54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f300c99459926efcebd5cacdab52ee0900534912b1c75db2556cfec826f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2867589a33d86d4239850bd34e12ff3064467a71264788d2dd5d807347b0f1c7`  
		Last Modified: Fri, 12 Apr 2024 16:00:25 GMT  
		Size: 27.3 MB (27331928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20240405`

```console
$ docker pull ubuntu@sha256:9bd295f67d19c9e4f8b7681d83a583f31b637184afb25e5138cc8ef50d1e344c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `ubuntu:mantic-20240405` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d2ef4d29f07d2e34e02bd3edbecd7e97c066a5ac1eddaf726d4dab7b4fd30abd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24887415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6f00029030e4f1fd73079a98f46caac7940db908032c0e53a2dd347ef6fa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a032cb47dd8d01b6383603fb581fd99c856b139e1a013415d969e9421b6803bc`  
		Last Modified: Fri, 12 Apr 2024 16:00:11 GMT  
		Size: 24.9 MB (24887415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240405` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1e4c25185533d7bed7864744d2a5b2c43bf1ac7a7f6427267c72828712e4e16a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be742dd48b8ce1c5254b2f75a0f28a5ad54d5cdffe7f198217d9f11618a8f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:942a35531af124aa3c3906d47e8dd6472cec1bfa9ec398abfea155f72c64cc96`  
		Last Modified: Fri, 12 Apr 2024 16:00:05 GMT  
		Size: 26.4 MB (26413454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240405` - linux; s390x

```console
$ docker pull ubuntu@sha256:fb8daccea84b4657e01ec61e5a1d9dbb75739c8096a2580f9ae1e379846feb54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f300c99459926efcebd5cacdab52ee0900534912b1c75db2556cfec826f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2867589a33d86d4239850bd34e12ff3064467a71264788d2dd5d807347b0f1c7`  
		Last Modified: Fri, 12 Apr 2024 16:00:25 GMT  
		Size: 27.3 MB (27331928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:f2e70beb6ac047e6424a1ee723777f63e4b9e636979e8e61609e31aa1fee5d10
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

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b61c7c7b34921e6805388eb4cd2bd7adb40f842af583c7af8eb28d3c50e6ea97
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27980097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa4940cd722b5042f615f16a268ba712e96f0be896c7dd0cf9310c545a5c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c7ec942a10b2818754e030a717ceb80881eef105a2efc304a3afeb2421e78c`  
		Last Modified: Sun, 07 Apr 2024 17:19:11 GMT  
		Size: 28.0 MB (27980097 bytes)  
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
$ docker pull ubuntu@sha256:63c1538627e447932daae84283e194b14c6323c16a29d9bdbe071e8744c5f0b4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f38b99e0ca2a6f55155893071f008bb5b14f2d2afb0a48ded1f22e085ccfcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf319107486d1a8ff3845cc8abca0de71f7437518fe348fce75fb7db345a555`  
		Last Modified: Sun, 07 Apr 2024 17:19:30 GMT  
		Size: 29.1 MB (29113387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240407.1`

```console
$ docker pull ubuntu@sha256:f2b38f9af9d7bc1815a2eb92ed34e1b5d5639b28c74060f3400a6ca70713b5a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `ubuntu:noble-20240407.1` - linux; arm variant v7

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

### `ubuntu:noble-20240407.1` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b61c7c7b34921e6805388eb4cd2bd7adb40f842af583c7af8eb28d3c50e6ea97
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27980097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa4940cd722b5042f615f16a268ba712e96f0be896c7dd0cf9310c545a5c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c7ec942a10b2818754e030a717ceb80881eef105a2efc304a3afeb2421e78c`  
		Last Modified: Sun, 07 Apr 2024 17:19:11 GMT  
		Size: 28.0 MB (27980097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240407.1` - linux; s390x

```console
$ docker pull ubuntu@sha256:63c1538627e447932daae84283e194b14c6323c16a29d9bdbe071e8744c5f0b4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f38b99e0ca2a6f55155893071f008bb5b14f2d2afb0a48ded1f22e085ccfcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf319107486d1a8ff3845cc8abca0de71f7437518fe348fce75fb7db345a555`  
		Last Modified: Sun, 07 Apr 2024 17:19:30 GMT  
		Size: 29.1 MB (29113387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:de75a9d421d24c1e335a0b1f8083be838c4652da43eb970348ce907f827236b7
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
$ docker pull ubuntu@sha256:d2ef4d29f07d2e34e02bd3edbecd7e97c066a5ac1eddaf726d4dab7b4fd30abd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24887415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6f00029030e4f1fd73079a98f46caac7940db908032c0e53a2dd347ef6fa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a032cb47dd8d01b6383603fb581fd99c856b139e1a013415d969e9421b6803bc`  
		Last Modified: Fri, 12 Apr 2024 16:00:11 GMT  
		Size: 24.9 MB (24887415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1e4c25185533d7bed7864744d2a5b2c43bf1ac7a7f6427267c72828712e4e16a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be742dd48b8ce1c5254b2f75a0f28a5ad54d5cdffe7f198217d9f11618a8f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:942a35531af124aa3c3906d47e8dd6472cec1bfa9ec398abfea155f72c64cc96`  
		Last Modified: Fri, 12 Apr 2024 16:00:05 GMT  
		Size: 26.4 MB (26413454 bytes)  
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
$ docker pull ubuntu@sha256:fb8daccea84b4657e01ec61e5a1d9dbb75739c8096a2580f9ae1e379846feb54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f300c99459926efcebd5cacdab52ee0900534912b1c75db2556cfec826f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2867589a33d86d4239850bd34e12ff3064467a71264788d2dd5d807347b0f1c7`  
		Last Modified: Fri, 12 Apr 2024 16:00:25 GMT  
		Size: 27.3 MB (27331928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
