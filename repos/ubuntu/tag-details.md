<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240123`](#ubuntufocal-20240123)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240212`](#ubuntujammy-20240212)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20240122`](#ubuntumantic-20240122)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240212`](#ubuntunoble-20240212)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:bb1c41682308d7040f74d103022816d41c50d7b0c89e9d706a74b4e548636e54
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
$ docker pull ubuntu@sha256:a4fab1802f08df089c4b2e0a1c8f1a06f573bd1775687d07fef4076d3a2e4900
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27514928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ca3f4297e795532c0d053ba443d392d5d316ee83ddee0de27f1e742a7db273`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c2a18cb8ae73adf18b9eb808a3e60fd6ad5c0ff3d3f38bec8f3bf46841d1d7ef
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b701af35d60a285f85ca02ccbff130ed7b830bd2c31661c3c80c05cd3da89c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7cb4aadc1d017fd0b959dbdb73cbf8f2c53c235380983c229e5ebf72bbe6f7f`  
		Last Modified: Tue, 23 Jan 2024 13:10:49 GMT  
		Size: 23.6 MB (23622522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:175ee225697a668b782a54a56f090c046584f06a93c1bae990972e4f1bf6e4ac
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25975597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b1498b9544ea65cbf02fb2feb0eea5a8af4f02097cb5447ec566061ff245c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b18d282303d00349baa5cbfbe46e187380241d41205df6b7d9a2e9b559ae4735
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49ecf9c2b1a4b41ec8b9daa07bb7b6a6da68ec765d4f08edfc1350c4adc64d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:7496a0e1418e0340b23bf80077c957059664b1f5298a1f96d39c5118acf11761
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26362871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be0b06e000c667996ac702818d0e6b46d3ef788f941a2ea91f039f57528c778`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c9202eb73d17302f2cc366ebffe022abacde01c41e47c6d408a29334a481207`  
		Last Modified: Tue, 23 Jan 2024 13:11:03 GMT  
		Size: 26.4 MB (26362871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:b5ca18f4a05446470d427e02b025f9d760dc95581f1d8f46a4091cca102171c9
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
$ docker pull ubuntu@sha256:81bba8d1dde7fc1883b6e95cd46d6c9f4874374f2b360c8db82620b33f6b5ca1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29536188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db8720ecbf5f5927d409cc61f9b4f7ffe23283917caaa992f847c4d83338cc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01007420e9b005dc14a8c8b0f996a2ad8e0d4af6c3d01e62f123be14fe48eec7`  
		Last Modified: Tue, 13 Feb 2024 10:22:22 GMT  
		Size: 29.5 MB (29536188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d3ea43ae1395f39a22db1706251310eb33f81c5589dfbcedee359a73a5083cd0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26634366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bc5703da420688253a2dbdff31de2fa4f2e47eb7a8409422be612ffcf10a5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:87abf73fc1c5bddcb97238e36e25996d6b676e1ad8a434aede39dc431524f9d4`  
		Last Modified: Thu, 25 Jan 2024 18:13:00 GMT  
		Size: 26.6 MB (26634366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ca165754e2f953a4f686409b1eb5855212f42a252462c9c50bbc3077f3b9a654
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27356877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50ab9f167975489853cbffd2be3bcadab3a9da27faf390ac48603c60d5c59e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2f00029acbafa8e205f18a167658ea1546d754e79641b667b77295f9e0e77766
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34503224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b8818f7bee0ebaa89bfbe389eb3513a31d67c8760ceacec07ba3af31c0c918`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4aad68167a35c53ced5a1c04f1766357ff1b620dec9d272c01720d4fb0d9558c`  
		Last Modified: Tue, 13 Feb 2024 10:22:40 GMT  
		Size: 34.5 MB (34503224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:66874e931f0e488d3d20b8276b98fa58476e537386cc893b464e2eb89de8cec8
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28008375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6188793d1e4a76920fb1ee814e268b6cb53fce69eaab58b272a15abfa5c9c7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8c305036370ece07999393ab52726bcdf8fc6cfdfaecfb9cb60f40ebaecec9e9`  
		Last Modified: Tue, 13 Feb 2024 10:22:46 GMT  
		Size: 28.0 MB (28008375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:f0bb9ee844f7adb284ac036a15469062adbe3a4458c06680216ed73df231cb31
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
$ docker pull ubuntu@sha256:496a9a44971eb4ac7aa9a218867b7eec98bdef452246c037aa206c841b653e08
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27272343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615f0aa2b7c0484e71159628f9979d7952c38e06f9f49c052fa4aafee9904d68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01889d9636d772424d3cf24aea681c992d26dc5199ddd7336dc043a28985710d`  
		Last Modified: Tue, 23 Jan 2024 13:26:21 GMT  
		Size: 27.3 MB (27272343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:01dac4a5a2a0a7fef6f130f323cc097fc4152f785120ccdf82958ba5237669b2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25206245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5249035258fbba600fda18f276638fe09c64a986b4de0455abd8a3c771df9e7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:693654547fc51f34d7707d19a966c27b1a03332c4a73850d61f678566f38f4d4`  
		Last Modified: Tue, 23 Jan 2024 13:26:34 GMT  
		Size: 25.2 MB (25206245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f2810774a67f175bb6b7ae44e4f1d617b41c592d6c7b5504236f44ea86a81601
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26398339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6659459dc389659ad62a22aa59f7fe3d989af7b558df2f35060e3e0622a3aea8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:156a77c81f1abbe7dc4d9fb1e0e7876b94be30c6369ef3391aa31a891420375a`  
		Last Modified: Tue, 23 Jan 2024 13:26:28 GMT  
		Size: 26.4 MB (26398339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:11f99d87fd59b9b9aa307ee360c7389a49d5d71e957f205234d0e9eacdaed05c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31349157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0509dbdce242c0743e9ba2f9d0199c6b0996ff7f30bb114db9f89a45ae5100`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:213adbfa59db3b5352aafb4a7b81f7dd77d1437299ff8860e037f17e717de9df`  
		Last Modified: Tue, 23 Jan 2024 13:26:40 GMT  
		Size: 31.3 MB (31349157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:85b606648d4614bf3d5030c0ece336b45224ee1b8f4f475e3495b6b3e00b7bbb
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27142659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8354d90088f3e18af817ff16b9e318588a005382e86751891140aa2218a210`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e066acab54e4d07067fc5a302b1eb8186e41b7017a393212ac61ba04db33aa66`  
		Last Modified: Tue, 23 Jan 2024 13:26:48 GMT  
		Size: 27.1 MB (27142659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:075eaee9ff69b3a935cc2190aa19a9c10310839189e80c610a95066efa90876a
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
$ docker pull ubuntu@sha256:72d82b0988f96de6621d825370677e51a3bfb8cdaaabe328a80dfea70c72f669
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29517629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85795990e70492c65df9fd1e61c2e3fa94ebe708c4b069332d136a43ec2e94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1e223e85e28d2d5352ebc3192c127de70ba77a6f66ebdcc9d6a999c7532d0832`  
		Last Modified: Mon, 12 Feb 2024 05:04:28 GMT  
		Size: 29.5 MB (29517629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0d1a1af8fb19296cb78f23e06fd84aaabb625d8bca4d4eebd8350c082d725656
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26745350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f234b39e0b110c911f32254eb44439a92ddd0634ec9acc88004b3bf9ded62fb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bf549e61b845c85dcc9dce843d1d2f0b25b08c8af68cb37363627a49004d4a23`  
		Last Modified: Sat, 27 Jan 2024 16:27:28 GMT  
		Size: 26.7 MB (26745350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:68b8d4d2d6f6b2ba3f5caf8293cfef6655bb1404c9f6d0643fd64c1ed26e1b45
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28581222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6914c26da3a2dd92c72669fb85c076c04c74860256015c727b2ed063a16136`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:06 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:09 GMT
ADD file:3ba739169a5d008e9474d4e0f02a874840e759fe8dd36ae68a5ccd1040648941 in / 
# Mon, 12 Feb 2024 04:52:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:51ae9e2de0523e4a824b7f66a17dc4e0006a01eccb52cad747fbf1b6fae0c6e2`  
		Last Modified: Mon, 12 Feb 2024 05:04:35 GMT  
		Size: 28.6 MB (28581222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b7204e85ced5a249ddecd08970688ca9af799f3134191149a6095f859839a078
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34132522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9398bce25bf86a68bc3d0abfe8850977f31db627a31587460656b960092606`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:54:47 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:54:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:54:50 GMT
ADD file:52a2f480522705b01ec516237a34993e5cb661cbb9082d50ffeb08b7f467770b in / 
# Mon, 12 Feb 2024 04:54:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:957d24e05868ff2566d16a7d2509244da1476eaa9d7c3a460f4878c4aa829c11`  
		Last Modified: Mon, 12 Feb 2024 05:04:48 GMT  
		Size: 34.1 MB (34132522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:33827e14a4ebccd3b5b7f051d2b8c51ffddc362bedac5e9000ccdb41cce0efdd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29723268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2a3a696b45390ef531fcdd4e1cbbae98e0bacf616b70e976e61a730217dc32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7529d682d403b448bed2284e8bb86bc179ff83938e0aa0aa5c8b18a51fa6dd8b`  
		Last Modified: Mon, 12 Feb 2024 05:04:54 GMT  
		Size: 29.7 MB (29723268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:075eaee9ff69b3a935cc2190aa19a9c10310839189e80c610a95066efa90876a
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
$ docker pull ubuntu@sha256:72d82b0988f96de6621d825370677e51a3bfb8cdaaabe328a80dfea70c72f669
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29517629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85795990e70492c65df9fd1e61c2e3fa94ebe708c4b069332d136a43ec2e94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1e223e85e28d2d5352ebc3192c127de70ba77a6f66ebdcc9d6a999c7532d0832`  
		Last Modified: Mon, 12 Feb 2024 05:04:28 GMT  
		Size: 29.5 MB (29517629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0d1a1af8fb19296cb78f23e06fd84aaabb625d8bca4d4eebd8350c082d725656
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26745350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f234b39e0b110c911f32254eb44439a92ddd0634ec9acc88004b3bf9ded62fb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bf549e61b845c85dcc9dce843d1d2f0b25b08c8af68cb37363627a49004d4a23`  
		Last Modified: Sat, 27 Jan 2024 16:27:28 GMT  
		Size: 26.7 MB (26745350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:68b8d4d2d6f6b2ba3f5caf8293cfef6655bb1404c9f6d0643fd64c1ed26e1b45
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28581222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6914c26da3a2dd92c72669fb85c076c04c74860256015c727b2ed063a16136`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:06 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:09 GMT
ADD file:3ba739169a5d008e9474d4e0f02a874840e759fe8dd36ae68a5ccd1040648941 in / 
# Mon, 12 Feb 2024 04:52:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:51ae9e2de0523e4a824b7f66a17dc4e0006a01eccb52cad747fbf1b6fae0c6e2`  
		Last Modified: Mon, 12 Feb 2024 05:04:35 GMT  
		Size: 28.6 MB (28581222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b7204e85ced5a249ddecd08970688ca9af799f3134191149a6095f859839a078
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34132522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9398bce25bf86a68bc3d0abfe8850977f31db627a31587460656b960092606`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:54:47 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:54:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:54:50 GMT
ADD file:52a2f480522705b01ec516237a34993e5cb661cbb9082d50ffeb08b7f467770b in / 
# Mon, 12 Feb 2024 04:54:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:957d24e05868ff2566d16a7d2509244da1476eaa9d7c3a460f4878c4aa829c11`  
		Last Modified: Mon, 12 Feb 2024 05:04:48 GMT  
		Size: 34.1 MB (34132522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:33827e14a4ebccd3b5b7f051d2b8c51ffddc362bedac5e9000ccdb41cce0efdd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29723268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2a3a696b45390ef531fcdd4e1cbbae98e0bacf616b70e976e61a730217dc32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7529d682d403b448bed2284e8bb86bc179ff83938e0aa0aa5c8b18a51fa6dd8b`  
		Last Modified: Mon, 12 Feb 2024 05:04:54 GMT  
		Size: 29.7 MB (29723268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:bb1c41682308d7040f74d103022816d41c50d7b0c89e9d706a74b4e548636e54
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
$ docker pull ubuntu@sha256:a4fab1802f08df089c4b2e0a1c8f1a06f573bd1775687d07fef4076d3a2e4900
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27514928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ca3f4297e795532c0d053ba443d392d5d316ee83ddee0de27f1e742a7db273`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c2a18cb8ae73adf18b9eb808a3e60fd6ad5c0ff3d3f38bec8f3bf46841d1d7ef
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b701af35d60a285f85ca02ccbff130ed7b830bd2c31661c3c80c05cd3da89c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7cb4aadc1d017fd0b959dbdb73cbf8f2c53c235380983c229e5ebf72bbe6f7f`  
		Last Modified: Tue, 23 Jan 2024 13:10:49 GMT  
		Size: 23.6 MB (23622522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:175ee225697a668b782a54a56f090c046584f06a93c1bae990972e4f1bf6e4ac
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25975597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b1498b9544ea65cbf02fb2feb0eea5a8af4f02097cb5447ec566061ff245c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b18d282303d00349baa5cbfbe46e187380241d41205df6b7d9a2e9b559ae4735
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49ecf9c2b1a4b41ec8b9daa07bb7b6a6da68ec765d4f08edfc1350c4adc64d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:7496a0e1418e0340b23bf80077c957059664b1f5298a1f96d39c5118acf11761
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26362871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be0b06e000c667996ac702818d0e6b46d3ef788f941a2ea91f039f57528c778`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c9202eb73d17302f2cc366ebffe022abacde01c41e47c6d408a29334a481207`  
		Last Modified: Tue, 23 Jan 2024 13:11:03 GMT  
		Size: 26.4 MB (26362871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240123`

```console
$ docker pull ubuntu@sha256:bb1c41682308d7040f74d103022816d41c50d7b0c89e9d706a74b4e548636e54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20240123` - linux; amd64

```console
$ docker pull ubuntu@sha256:a4fab1802f08df089c4b2e0a1c8f1a06f573bd1775687d07fef4076d3a2e4900
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27514928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ca3f4297e795532c0d053ba443d392d5d316ee83ddee0de27f1e742a7db273`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240123` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c2a18cb8ae73adf18b9eb808a3e60fd6ad5c0ff3d3f38bec8f3bf46841d1d7ef
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b701af35d60a285f85ca02ccbff130ed7b830bd2c31661c3c80c05cd3da89c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7cb4aadc1d017fd0b959dbdb73cbf8f2c53c235380983c229e5ebf72bbe6f7f`  
		Last Modified: Tue, 23 Jan 2024 13:10:49 GMT  
		Size: 23.6 MB (23622522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240123` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:175ee225697a668b782a54a56f090c046584f06a93c1bae990972e4f1bf6e4ac
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25975597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b1498b9544ea65cbf02fb2feb0eea5a8af4f02097cb5447ec566061ff245c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240123` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b18d282303d00349baa5cbfbe46e187380241d41205df6b7d9a2e9b559ae4735
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49ecf9c2b1a4b41ec8b9daa07bb7b6a6da68ec765d4f08edfc1350c4adc64d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240123` - linux; s390x

```console
$ docker pull ubuntu@sha256:7496a0e1418e0340b23bf80077c957059664b1f5298a1f96d39c5118acf11761
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26362871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be0b06e000c667996ac702818d0e6b46d3ef788f941a2ea91f039f57528c778`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c9202eb73d17302f2cc366ebffe022abacde01c41e47c6d408a29334a481207`  
		Last Modified: Tue, 23 Jan 2024 13:11:03 GMT  
		Size: 26.4 MB (26362871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:b5ca18f4a05446470d427e02b025f9d760dc95581f1d8f46a4091cca102171c9
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
$ docker pull ubuntu@sha256:81bba8d1dde7fc1883b6e95cd46d6c9f4874374f2b360c8db82620b33f6b5ca1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29536188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db8720ecbf5f5927d409cc61f9b4f7ffe23283917caaa992f847c4d83338cc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01007420e9b005dc14a8c8b0f996a2ad8e0d4af6c3d01e62f123be14fe48eec7`  
		Last Modified: Tue, 13 Feb 2024 10:22:22 GMT  
		Size: 29.5 MB (29536188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d3ea43ae1395f39a22db1706251310eb33f81c5589dfbcedee359a73a5083cd0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26634366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bc5703da420688253a2dbdff31de2fa4f2e47eb7a8409422be612ffcf10a5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:87abf73fc1c5bddcb97238e36e25996d6b676e1ad8a434aede39dc431524f9d4`  
		Last Modified: Thu, 25 Jan 2024 18:13:00 GMT  
		Size: 26.6 MB (26634366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ca165754e2f953a4f686409b1eb5855212f42a252462c9c50bbc3077f3b9a654
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27356877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50ab9f167975489853cbffd2be3bcadab3a9da27faf390ac48603c60d5c59e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2f00029acbafa8e205f18a167658ea1546d754e79641b667b77295f9e0e77766
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34503224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b8818f7bee0ebaa89bfbe389eb3513a31d67c8760ceacec07ba3af31c0c918`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4aad68167a35c53ced5a1c04f1766357ff1b620dec9d272c01720d4fb0d9558c`  
		Last Modified: Tue, 13 Feb 2024 10:22:40 GMT  
		Size: 34.5 MB (34503224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:66874e931f0e488d3d20b8276b98fa58476e537386cc893b464e2eb89de8cec8
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28008375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6188793d1e4a76920fb1ee814e268b6cb53fce69eaab58b272a15abfa5c9c7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8c305036370ece07999393ab52726bcdf8fc6cfdfaecfb9cb60f40ebaecec9e9`  
		Last Modified: Tue, 13 Feb 2024 10:22:46 GMT  
		Size: 28.0 MB (28008375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240212`

```console
$ docker pull ubuntu@sha256:da61bc7cb887ba56c4f857b1a0fb5e2520e2b2051e4b04904ee21a789e385182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20240212` - linux; amd64

```console
$ docker pull ubuntu@sha256:81bba8d1dde7fc1883b6e95cd46d6c9f4874374f2b360c8db82620b33f6b5ca1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29536188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db8720ecbf5f5927d409cc61f9b4f7ffe23283917caaa992f847c4d83338cc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01007420e9b005dc14a8c8b0f996a2ad8e0d4af6c3d01e62f123be14fe48eec7`  
		Last Modified: Tue, 13 Feb 2024 10:22:22 GMT  
		Size: 29.5 MB (29536188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240212` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ca165754e2f953a4f686409b1eb5855212f42a252462c9c50bbc3077f3b9a654
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27356877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50ab9f167975489853cbffd2be3bcadab3a9da27faf390ac48603c60d5c59e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240212` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2f00029acbafa8e205f18a167658ea1546d754e79641b667b77295f9e0e77766
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34503224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b8818f7bee0ebaa89bfbe389eb3513a31d67c8760ceacec07ba3af31c0c918`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4aad68167a35c53ced5a1c04f1766357ff1b620dec9d272c01720d4fb0d9558c`  
		Last Modified: Tue, 13 Feb 2024 10:22:40 GMT  
		Size: 34.5 MB (34503224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240212` - linux; s390x

```console
$ docker pull ubuntu@sha256:66874e931f0e488d3d20b8276b98fa58476e537386cc893b464e2eb89de8cec8
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28008375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6188793d1e4a76920fb1ee814e268b6cb53fce69eaab58b272a15abfa5c9c7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8c305036370ece07999393ab52726bcdf8fc6cfdfaecfb9cb60f40ebaecec9e9`  
		Last Modified: Tue, 13 Feb 2024 10:22:46 GMT  
		Size: 28.0 MB (28008375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:b5ca18f4a05446470d427e02b025f9d760dc95581f1d8f46a4091cca102171c9
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
$ docker pull ubuntu@sha256:81bba8d1dde7fc1883b6e95cd46d6c9f4874374f2b360c8db82620b33f6b5ca1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29536188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db8720ecbf5f5927d409cc61f9b4f7ffe23283917caaa992f847c4d83338cc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01007420e9b005dc14a8c8b0f996a2ad8e0d4af6c3d01e62f123be14fe48eec7`  
		Last Modified: Tue, 13 Feb 2024 10:22:22 GMT  
		Size: 29.5 MB (29536188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d3ea43ae1395f39a22db1706251310eb33f81c5589dfbcedee359a73a5083cd0
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26634366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bc5703da420688253a2dbdff31de2fa4f2e47eb7a8409422be612ffcf10a5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:87abf73fc1c5bddcb97238e36e25996d6b676e1ad8a434aede39dc431524f9d4`  
		Last Modified: Thu, 25 Jan 2024 18:13:00 GMT  
		Size: 26.6 MB (26634366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ca165754e2f953a4f686409b1eb5855212f42a252462c9c50bbc3077f3b9a654
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27356877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50ab9f167975489853cbffd2be3bcadab3a9da27faf390ac48603c60d5c59e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2f00029acbafa8e205f18a167658ea1546d754e79641b667b77295f9e0e77766
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34503224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b8818f7bee0ebaa89bfbe389eb3513a31d67c8760ceacec07ba3af31c0c918`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4aad68167a35c53ced5a1c04f1766357ff1b620dec9d272c01720d4fb0d9558c`  
		Last Modified: Tue, 13 Feb 2024 10:22:40 GMT  
		Size: 34.5 MB (34503224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:66874e931f0e488d3d20b8276b98fa58476e537386cc893b464e2eb89de8cec8
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28008375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6188793d1e4a76920fb1ee814e268b6cb53fce69eaab58b272a15abfa5c9c7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8c305036370ece07999393ab52726bcdf8fc6cfdfaecfb9cb60f40ebaecec9e9`  
		Last Modified: Tue, 13 Feb 2024 10:22:46 GMT  
		Size: 28.0 MB (28008375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:f0bb9ee844f7adb284ac036a15469062adbe3a4458c06680216ed73df231cb31
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
$ docker pull ubuntu@sha256:496a9a44971eb4ac7aa9a218867b7eec98bdef452246c037aa206c841b653e08
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27272343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615f0aa2b7c0484e71159628f9979d7952c38e06f9f49c052fa4aafee9904d68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01889d9636d772424d3cf24aea681c992d26dc5199ddd7336dc043a28985710d`  
		Last Modified: Tue, 23 Jan 2024 13:26:21 GMT  
		Size: 27.3 MB (27272343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:01dac4a5a2a0a7fef6f130f323cc097fc4152f785120ccdf82958ba5237669b2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25206245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5249035258fbba600fda18f276638fe09c64a986b4de0455abd8a3c771df9e7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:693654547fc51f34d7707d19a966c27b1a03332c4a73850d61f678566f38f4d4`  
		Last Modified: Tue, 23 Jan 2024 13:26:34 GMT  
		Size: 25.2 MB (25206245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f2810774a67f175bb6b7ae44e4f1d617b41c592d6c7b5504236f44ea86a81601
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26398339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6659459dc389659ad62a22aa59f7fe3d989af7b558df2f35060e3e0622a3aea8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:156a77c81f1abbe7dc4d9fb1e0e7876b94be30c6369ef3391aa31a891420375a`  
		Last Modified: Tue, 23 Jan 2024 13:26:28 GMT  
		Size: 26.4 MB (26398339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:11f99d87fd59b9b9aa307ee360c7389a49d5d71e957f205234d0e9eacdaed05c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31349157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0509dbdce242c0743e9ba2f9d0199c6b0996ff7f30bb114db9f89a45ae5100`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:213adbfa59db3b5352aafb4a7b81f7dd77d1437299ff8860e037f17e717de9df`  
		Last Modified: Tue, 23 Jan 2024 13:26:40 GMT  
		Size: 31.3 MB (31349157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:85b606648d4614bf3d5030c0ece336b45224ee1b8f4f475e3495b6b3e00b7bbb
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27142659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8354d90088f3e18af817ff16b9e318588a005382e86751891140aa2218a210`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e066acab54e4d07067fc5a302b1eb8186e41b7017a393212ac61ba04db33aa66`  
		Last Modified: Tue, 23 Jan 2024 13:26:48 GMT  
		Size: 27.1 MB (27142659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20240122`

```console
$ docker pull ubuntu@sha256:f0bb9ee844f7adb284ac036a15469062adbe3a4458c06680216ed73df231cb31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20240122` - linux; amd64

```console
$ docker pull ubuntu@sha256:496a9a44971eb4ac7aa9a218867b7eec98bdef452246c037aa206c841b653e08
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27272343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615f0aa2b7c0484e71159628f9979d7952c38e06f9f49c052fa4aafee9904d68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01889d9636d772424d3cf24aea681c992d26dc5199ddd7336dc043a28985710d`  
		Last Modified: Tue, 23 Jan 2024 13:26:21 GMT  
		Size: 27.3 MB (27272343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240122` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:01dac4a5a2a0a7fef6f130f323cc097fc4152f785120ccdf82958ba5237669b2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25206245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5249035258fbba600fda18f276638fe09c64a986b4de0455abd8a3c771df9e7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:693654547fc51f34d7707d19a966c27b1a03332c4a73850d61f678566f38f4d4`  
		Last Modified: Tue, 23 Jan 2024 13:26:34 GMT  
		Size: 25.2 MB (25206245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240122` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f2810774a67f175bb6b7ae44e4f1d617b41c592d6c7b5504236f44ea86a81601
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26398339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6659459dc389659ad62a22aa59f7fe3d989af7b558df2f35060e3e0622a3aea8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:156a77c81f1abbe7dc4d9fb1e0e7876b94be30c6369ef3391aa31a891420375a`  
		Last Modified: Tue, 23 Jan 2024 13:26:28 GMT  
		Size: 26.4 MB (26398339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240122` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:11f99d87fd59b9b9aa307ee360c7389a49d5d71e957f205234d0e9eacdaed05c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31349157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0509dbdce242c0743e9ba2f9d0199c6b0996ff7f30bb114db9f89a45ae5100`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:213adbfa59db3b5352aafb4a7b81f7dd77d1437299ff8860e037f17e717de9df`  
		Last Modified: Tue, 23 Jan 2024 13:26:40 GMT  
		Size: 31.3 MB (31349157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240122` - linux; s390x

```console
$ docker pull ubuntu@sha256:85b606648d4614bf3d5030c0ece336b45224ee1b8f4f475e3495b6b3e00b7bbb
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27142659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8354d90088f3e18af817ff16b9e318588a005382e86751891140aa2218a210`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e066acab54e4d07067fc5a302b1eb8186e41b7017a393212ac61ba04db33aa66`  
		Last Modified: Tue, 23 Jan 2024 13:26:48 GMT  
		Size: 27.1 MB (27142659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:075eaee9ff69b3a935cc2190aa19a9c10310839189e80c610a95066efa90876a
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
$ docker pull ubuntu@sha256:72d82b0988f96de6621d825370677e51a3bfb8cdaaabe328a80dfea70c72f669
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29517629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85795990e70492c65df9fd1e61c2e3fa94ebe708c4b069332d136a43ec2e94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1e223e85e28d2d5352ebc3192c127de70ba77a6f66ebdcc9d6a999c7532d0832`  
		Last Modified: Mon, 12 Feb 2024 05:04:28 GMT  
		Size: 29.5 MB (29517629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0d1a1af8fb19296cb78f23e06fd84aaabb625d8bca4d4eebd8350c082d725656
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26745350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f234b39e0b110c911f32254eb44439a92ddd0634ec9acc88004b3bf9ded62fb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bf549e61b845c85dcc9dce843d1d2f0b25b08c8af68cb37363627a49004d4a23`  
		Last Modified: Sat, 27 Jan 2024 16:27:28 GMT  
		Size: 26.7 MB (26745350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:68b8d4d2d6f6b2ba3f5caf8293cfef6655bb1404c9f6d0643fd64c1ed26e1b45
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28581222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6914c26da3a2dd92c72669fb85c076c04c74860256015c727b2ed063a16136`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:06 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:09 GMT
ADD file:3ba739169a5d008e9474d4e0f02a874840e759fe8dd36ae68a5ccd1040648941 in / 
# Mon, 12 Feb 2024 04:52:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:51ae9e2de0523e4a824b7f66a17dc4e0006a01eccb52cad747fbf1b6fae0c6e2`  
		Last Modified: Mon, 12 Feb 2024 05:04:35 GMT  
		Size: 28.6 MB (28581222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b7204e85ced5a249ddecd08970688ca9af799f3134191149a6095f859839a078
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34132522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9398bce25bf86a68bc3d0abfe8850977f31db627a31587460656b960092606`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:54:47 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:54:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:54:50 GMT
ADD file:52a2f480522705b01ec516237a34993e5cb661cbb9082d50ffeb08b7f467770b in / 
# Mon, 12 Feb 2024 04:54:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:957d24e05868ff2566d16a7d2509244da1476eaa9d7c3a460f4878c4aa829c11`  
		Last Modified: Mon, 12 Feb 2024 05:04:48 GMT  
		Size: 34.1 MB (34132522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:33827e14a4ebccd3b5b7f051d2b8c51ffddc362bedac5e9000ccdb41cce0efdd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29723268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2a3a696b45390ef531fcdd4e1cbbae98e0bacf616b70e976e61a730217dc32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7529d682d403b448bed2284e8bb86bc179ff83938e0aa0aa5c8b18a51fa6dd8b`  
		Last Modified: Mon, 12 Feb 2024 05:04:54 GMT  
		Size: 29.7 MB (29723268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240212`

```console
$ docker pull ubuntu@sha256:53fee4838dbae7523648ef9f28d8ed8b29ffd17417c4f234a18e68776fb32404
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble-20240212` - linux; amd64

```console
$ docker pull ubuntu@sha256:72d82b0988f96de6621d825370677e51a3bfb8cdaaabe328a80dfea70c72f669
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29517629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85795990e70492c65df9fd1e61c2e3fa94ebe708c4b069332d136a43ec2e94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1e223e85e28d2d5352ebc3192c127de70ba77a6f66ebdcc9d6a999c7532d0832`  
		Last Modified: Mon, 12 Feb 2024 05:04:28 GMT  
		Size: 29.5 MB (29517629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240212` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:68b8d4d2d6f6b2ba3f5caf8293cfef6655bb1404c9f6d0643fd64c1ed26e1b45
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28581222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6914c26da3a2dd92c72669fb85c076c04c74860256015c727b2ed063a16136`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:06 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:09 GMT
ADD file:3ba739169a5d008e9474d4e0f02a874840e759fe8dd36ae68a5ccd1040648941 in / 
# Mon, 12 Feb 2024 04:52:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:51ae9e2de0523e4a824b7f66a17dc4e0006a01eccb52cad747fbf1b6fae0c6e2`  
		Last Modified: Mon, 12 Feb 2024 05:04:35 GMT  
		Size: 28.6 MB (28581222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240212` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b7204e85ced5a249ddecd08970688ca9af799f3134191149a6095f859839a078
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34132522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9398bce25bf86a68bc3d0abfe8850977f31db627a31587460656b960092606`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:54:47 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:54:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:54:50 GMT
ADD file:52a2f480522705b01ec516237a34993e5cb661cbb9082d50ffeb08b7f467770b in / 
# Mon, 12 Feb 2024 04:54:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:957d24e05868ff2566d16a7d2509244da1476eaa9d7c3a460f4878c4aa829c11`  
		Last Modified: Mon, 12 Feb 2024 05:04:48 GMT  
		Size: 34.1 MB (34132522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240212` - linux; s390x

```console
$ docker pull ubuntu@sha256:33827e14a4ebccd3b5b7f051d2b8c51ffddc362bedac5e9000ccdb41cce0efdd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29723268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2a3a696b45390ef531fcdd4e1cbbae98e0bacf616b70e976e61a730217dc32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7529d682d403b448bed2284e8bb86bc179ff83938e0aa0aa5c8b18a51fa6dd8b`  
		Last Modified: Mon, 12 Feb 2024 05:04:54 GMT  
		Size: 29.7 MB (29723268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:f0bb9ee844f7adb284ac036a15469062adbe3a4458c06680216ed73df231cb31
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
$ docker pull ubuntu@sha256:496a9a44971eb4ac7aa9a218867b7eec98bdef452246c037aa206c841b653e08
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27272343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615f0aa2b7c0484e71159628f9979d7952c38e06f9f49c052fa4aafee9904d68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01889d9636d772424d3cf24aea681c992d26dc5199ddd7336dc043a28985710d`  
		Last Modified: Tue, 23 Jan 2024 13:26:21 GMT  
		Size: 27.3 MB (27272343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:01dac4a5a2a0a7fef6f130f323cc097fc4152f785120ccdf82958ba5237669b2
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25206245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5249035258fbba600fda18f276638fe09c64a986b4de0455abd8a3c771df9e7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:693654547fc51f34d7707d19a966c27b1a03332c4a73850d61f678566f38f4d4`  
		Last Modified: Tue, 23 Jan 2024 13:26:34 GMT  
		Size: 25.2 MB (25206245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f2810774a67f175bb6b7ae44e4f1d617b41c592d6c7b5504236f44ea86a81601
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26398339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6659459dc389659ad62a22aa59f7fe3d989af7b558df2f35060e3e0622a3aea8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:156a77c81f1abbe7dc4d9fb1e0e7876b94be30c6369ef3391aa31a891420375a`  
		Last Modified: Tue, 23 Jan 2024 13:26:28 GMT  
		Size: 26.4 MB (26398339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:11f99d87fd59b9b9aa307ee360c7389a49d5d71e957f205234d0e9eacdaed05c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31349157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0509dbdce242c0743e9ba2f9d0199c6b0996ff7f30bb114db9f89a45ae5100`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:213adbfa59db3b5352aafb4a7b81f7dd77d1437299ff8860e037f17e717de9df`  
		Last Modified: Tue, 23 Jan 2024 13:26:40 GMT  
		Size: 31.3 MB (31349157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:85b606648d4614bf3d5030c0ece336b45224ee1b8f4f475e3495b6b3e00b7bbb
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27142659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8354d90088f3e18af817ff16b9e318588a005382e86751891140aa2218a210`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e066acab54e4d07067fc5a302b1eb8186e41b7017a393212ac61ba04db33aa66`  
		Last Modified: Tue, 23 Jan 2024 13:26:48 GMT  
		Size: 27.1 MB (27142659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
