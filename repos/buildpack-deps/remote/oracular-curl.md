## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:604c67637d545064acd57022f6acb419811feca56b355372cfebc1b73fcccf2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b49b76bb576b4b3fc4f23701ee0a02bbbcb8eae159af9437c5f38f8178785c6e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50344523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d4f2a21fc37da45dbb4b161dce07c77ba261fc392b03124a232a0bf44f592f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:58 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:00 GMT
ADD file:e0e1920c83dbb04acc51e3cea2d1100f9149baca28e8f9ca859721b92a00c661 in / 
# Fri, 13 Sep 2024 03:45:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8cdc21141b65ce4bcb1fda37d4d022dae065e029a30e7bf520c22f0a695a9634`  
		Last Modified: Tue, 17 Sep 2024 00:53:01 GMT  
		Size: 35.0 MB (35037517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b855f4b2872c5cc776792754e4a57964c452aaaa6fa69c1a8bc9ed3d1bf6ee`  
		Last Modified: Tue, 17 Sep 2024 00:52:59 GMT  
		Size: 15.3 MB (15307006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9446ee61f995f3dfc1fa728f233d2da1e5b24ff028ba8167889404204dae903f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44382464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a2f3f82859bdc8b1634c4aade93ae6077a54f750a95e27fc7fad3b4c49200f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:54 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:58 GMT
ADD file:4a74176688f6256cc90d758b02955eb55de176831a5890c949712ad4b2991476 in / 
# Sun, 11 Aug 2024 15:38:58 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba000785763e277141f722f9cc6aebee15ac21572de15075a6407026d2ceab7c`  
		Last Modified: Sat, 07 Sep 2024 02:05:11 GMT  
		Size: 28.2 MB (28151027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693d4bfd023e08a42b470cb0b43c766b88b85f7f30fb5b43fa0219943ce2a3c9`  
		Last Modified: Sat, 07 Sep 2024 02:05:08 GMT  
		Size: 16.2 MB (16231437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8e16dd7f2df32674bb26fcabbccdd1ccf59e55d9edd2c012c3237719aa906c11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49330826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ad42c1592da0f50a51ac84647eb333e07ccedc14104a52d63a2927c8738660`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:41 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:43 GMT
ADD file:1ad5462522bfc6d8b07f9d64ddf868aa9145c44d7e36ac7489e07719bc0f9c50 in / 
# Sun, 11 Aug 2024 15:38:43 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dc0f8ac147f52f41cac91af40556dcda467531813bfbe1899f174f25d02e853c`  
		Last Modified: Tue, 20 Aug 2024 05:04:56 GMT  
		Size: 31.0 MB (31036287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12168fbcdb069935dfac3395cf822dcc16837e5f6b7f9c66bb10e5975d6ac3ea`  
		Last Modified: Sat, 07 Sep 2024 04:25:43 GMT  
		Size: 18.3 MB (18294539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c31ef5cefc510370fd2e0d41f558d4a381ecade8e7168378ee6bc5d0309e33e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56889642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0792239655ab9185bcd0a45c457efa02d805aa08515f9b3acaaf76d9fbd01bf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:23 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:27 GMT
ADD file:5e35a64fdad21cdf96e70998641a823422343cb6ea2010b118d6476fab494360 in / 
# Fri, 13 Sep 2024 03:45:27 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4888f88bee4723604514eb67de9747f97c48812938a294f52e966dcad4b9cce1`  
		Last Modified: Tue, 17 Sep 2024 00:54:26 GMT  
		Size: 39.7 MB (39707210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258f534636942cc44347387dfeec93cb3a51718f6b960d8eb5b1db05d18bc53`  
		Last Modified: Tue, 17 Sep 2024 00:54:21 GMT  
		Size: 17.2 MB (17182432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8bae7a8936a258e09c7dbc700fba9509253561b417d46f360568eb7ce5cf2dd1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50989867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb7c2e96d5d09c84c81980bacf3e84aeb009013a6a49e807a620bd0f9b6ded8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:53:15 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:53:16 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:53:46 GMT
ADD file:456f458279dbf8e3c880562bb6c249e83ce6b17f95c004e173c314809ef77c92 in / 
# Sun, 11 Aug 2024 15:53:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 14:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e6ada0e2c161b5121d9519696516cf03e7fe74dd064fab2e287b03e1ea53c60`  
		Last Modified: Tue, 20 Aug 2024 03:32:11 GMT  
		Size: 32.5 MB (32490296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b351c7c752d081674b0efaec97a401d9b590bfb4801154cd82ce0f93d6f53bc`  
		Last Modified: Sat, 07 Sep 2024 14:34:21 GMT  
		Size: 18.5 MB (18499571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2fcf7b518d8c311ccc0e0622d08cb0e97d47626ef630f5234913688c7bd5bdcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50544097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6014a89ccf41a15552b52943eeaf557fbde2b8420cf3c6aa990c1d72fe143f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:23 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:25 GMT
ADD file:1afe7006fc30d35d19a6fd7338d9bdf3312fb2e5d9c617c709d1a2edc626d881 in / 
# Sun, 11 Aug 2024 15:38:25 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29e8b1ec75570fb19b7a0386180396a0e815ede57a87574c2ad028bfecdd6918`  
		Last Modified: Sat, 07 Sep 2024 01:56:24 GMT  
		Size: 31.1 MB (31132029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70745f7dad6d5386030f49f2426f299968336739bcbcf9ae2b8462560b4a9943`  
		Last Modified: Sat, 07 Sep 2024 01:56:23 GMT  
		Size: 19.4 MB (19412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
