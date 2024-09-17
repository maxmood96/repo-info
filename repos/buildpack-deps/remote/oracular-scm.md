## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:4b6e03901b9d39658f70d7b0d18dea2818a20dd098d2db04447a5026eb2d0c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1dbfd363c7265b73108465a8d3d29f0f9f581cb47beaad4ea0b3401cc66bad85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97162065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11d235b4586dfae5f82c5113a4bcc2c2f300aec0770c713922eb195365e78a0`
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
# Tue, 17 Sep 2024 00:48:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:16ebac33bb0b35e8874ec506bbc4ce286511296d30234e78372cf6cdb13cbb27`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 46.8 MB (46817542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e8115839661ba0860f523aa5dc52f0996d50bcb66b7dac2426d3751c1e707d8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94182218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f4879bc17f4cedf51f9ea3f3d7f92f600b6ea5c8b1a4fd668ed36f0e115c00`
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
# Sat, 07 Sep 2024 02:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:3ff511081b01199e4b9bb12d45bce6d56e4cd79db917542973d713b209bc166e`  
		Last Modified: Sat, 07 Sep 2024 02:05:26 GMT  
		Size: 49.8 MB (49799754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:94264f92b0f40c54d2d0121c7e8282be78c7206938df364c29001ce97906a396
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96133127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d209bc091e3256b3bff604f86e7403d54ecb16f4b2fa2b7ad38897c19c0b6e`
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
# Sat, 07 Sep 2024 04:20:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:3024e10b71baa355a2df6e0d250585dc206f2c9ea54534441463dc57467b4b44`  
		Last Modified: Sat, 07 Sep 2024 04:25:59 GMT  
		Size: 46.8 MB (46802301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d6c7636a492027cadedc80b2be66033e88bcb71afbfb869d1399a6e8bed8e49a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109044474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9076d4d7af26071c76e0e56979ffaf8e0a166374403bcb86b9496ffdfb4237e8`
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
# Tue, 17 Sep 2024 00:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:d032b3cccdd32b4010c1af161c1a432b31b8a95216f55327e02c652bd9616d31`  
		Last Modified: Tue, 17 Sep 2024 00:54:43 GMT  
		Size: 52.2 MB (52154832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:35613709acc4ea8bcfcfa6d711b2271dff5b9e120bb8c0b6c6dac2f8c34db151
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105976589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419577b50cc157b961183f2aaabbfe0f6b7a081e371798751ed9b9e2c1e3f3a`
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
# Sat, 07 Sep 2024 14:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:2241754e98cf7884cc7b38dc30666fa15dfe2c846239595a26f28fa0792b730c`  
		Last Modified: Sat, 07 Sep 2024 14:35:33 GMT  
		Size: 55.0 MB (54986722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2545f66cce61aa3a51ae66a8bcaafadbb8ee5d314962d0685d527fc728e0789e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98801086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70d9ba9e6a60f35a439d147379eedbda2b8b7b38e0e792c52f8935c0ea6277f`
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
# Sat, 07 Sep 2024 01:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:008cf182f449632ffe2a4d63ef9fa22ab66fd95d2c395d89ba25703628dae55b`  
		Last Modified: Sat, 07 Sep 2024 01:56:36 GMT  
		Size: 48.3 MB (48256989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
