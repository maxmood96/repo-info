## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:c0e87e100c09d21d8e8221c830c77281be192018f0054faed074f13efac7d44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3d3bc676bc8330dfbdb1ba49f7db0e4e9d5ec35f842f6d899dbd7c98b70148c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90034756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa383e20236dd961851f819da3c9a87c5502cd1b608efd12261092ca851b2e35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:41:37 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:41:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:41:40 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 10 Oct 2024 07:41:40 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:40:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b5ff6f3bf8380732596c0d88127072ad3ade77c0b660a419be02e5b74d17b`  
		Last Modified: Fri, 11 Oct 2024 23:48:39 GMT  
		Size: 13.6 MB (13617675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e923f23d6111f25a1ed5c513699e6b8610c1fd3541c8d558e4a047f92cf79e`  
		Last Modified: Fri, 11 Oct 2024 23:48:54 GMT  
		Size: 45.8 MB (45803803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9c4169651c7eb780e88ca963304e534f9af1a8dfa37e9ef971cc25363075b0dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89809169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8948e5895e473ca8c95b7b58d5394c2e60c7d77561f28920e00f2ff53795f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:40 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:41 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:43:43 GMT
ADD file:a30667697f58d730cc31ae308b1ba41bf25987733d14114fca71a90447988801 in / 
# Thu, 10 Oct 2024 07:43:44 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 00:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ebc4eee72d0a91a5a59ea1b60758bd4ff0e56e71e15430000cf9a33bd0b45ca2`  
		Last Modified: Sat, 12 Oct 2024 00:33:04 GMT  
		Size: 27.7 MB (27734482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4569d89fe8b49f32a79c828326d80ca875082c0fac286d85ca20d5e42d607adb`  
		Last Modified: Sat, 12 Oct 2024 00:44:56 GMT  
		Size: 12.8 MB (12775066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21917cb06aed5df1c331e743825da573c40b65970048da822fc836b0c3cbb5c`  
		Last Modified: Sat, 12 Oct 2024 00:45:10 GMT  
		Size: 49.3 MB (49299621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4a061d51336e3f8d6443253f8da33c4879626f6bb51547e22bf23f3bfb01997e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89175579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fc3e30f1a7a96236a28d9aca0b0cc90568b5363cc113711cf899e48afe84f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:44:36 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:44:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:39 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 10 Oct 2024 07:44:40 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:58:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2774e2077824bb6f6c4d20aba3eb095083efde5131d2b61d94e9cb99d548b6`  
		Last Modified: Sat, 12 Oct 2024 00:07:47 GMT  
		Size: 13.5 MB (13453285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6173824c2652a82d7289eedb2df956fa90acadda3114bf4b1ca0b7092e1186`  
		Last Modified: Sat, 12 Oct 2024 00:08:02 GMT  
		Size: 45.8 MB (45768708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a5be26f3f4431e054faa09b8c1f6ff5c044a3c2f311128c868ae6ba3ade9d87d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102531857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28988c2e6da5f7c623df5870961ae141d65f8696b6cc6d0634b022cb1bfda5d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:56 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:00 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 10 Oct 2024 07:44:00 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Fri, 11 Oct 2024 23:37:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:870d99e54f9cdff4b5ba4448d967491786519e8cbf54f10bd271e5dd32285ceb`  
		Last Modified: Fri, 11 Oct 2024 23:47:07 GMT  
		Size: 35.5 MB (35513269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c849c5c10301132208a8a8eb256192428c2e1559d2ce14590adb9fd1b2f0dec`  
		Last Modified: Fri, 11 Oct 2024 23:47:04 GMT  
		Size: 16.0 MB (15991319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb583f9c2bce7f331747939dae9021e4434772a15a2b859f64613f61ad2db69`  
		Last Modified: Fri, 11 Oct 2024 23:47:23 GMT  
		Size: 51.0 MB (51027269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:955b92a64c2705ac9f2b64a1eed54e334385090ba2561d6d27eed73aa093836a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100546656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c652ba17deed5b34f802fc0f37b68eccd4f8b0ffd45e4abe9b481011a01955e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Oct 2024 08:00:35 GMT
ARG RELEASE
# Thu, 10 Oct 2024 08:00:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 08:00:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 08:00:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 08:01:08 GMT
ADD file:99dcd7c18deec130fc01c654fb5a1f32f7e2a45fc9fc4a34112760a14e42cd1e in / 
# Thu, 10 Oct 2024 08:01:11 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:02:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 12 Oct 2024 08:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7903fd93c0f199630b946e3d8e9e18c502a30d3ce368061fffdd7ff86b68309c`  
		Last Modified: Sat, 12 Oct 2024 08:22:23 GMT  
		Size: 31.9 MB (31945588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428e08e6e0f7a9da26eecf6a7695dda4a20901e27b9d202db49a976836228acc`  
		Last Modified: Sat, 12 Oct 2024 08:22:10 GMT  
		Size: 14.3 MB (14321246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1be2f67bc54a669113de356e0864a1f7aa5e59b9d5fe4856d34ad8e94e8af58`  
		Last Modified: Sat, 12 Oct 2024 08:23:18 GMT  
		Size: 54.3 MB (54279822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:670d048ac22ccac1fed74cfb5714c7e94b6258c1efc866c41da1395b3a26b83a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92700086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66fe8c0be99d7249a1f123ad94ec058fcd4204c0c34167e176e2edebcbe287a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:28 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:29 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Fri, 11 Oct 2024 03:48:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97babcf495d74dff8479c7173a459ffe71f3e6016a2917626a2902468e3d22ce`  
		Last Modified: Wed, 16 Oct 2024 01:17:42 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fe4420f7cc31e2e71a763e82cb5891ae4caf5f1904fbbe4513bb4cd423b516`  
		Last Modified: Wed, 16 Oct 2024 01:17:57 GMT  
		Size: 47.1 MB (47062541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
