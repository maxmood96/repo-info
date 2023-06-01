## `buildpack-deps:bionic-scm`

```console
$ docker pull buildpack-deps@sha256:1cab4ecbce66fc999867933ec7534fd63f78f422a8a8a83d6281197248f9dbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7eeaf337a3fd7ba76486e2d2cffb79b8b154cd54c1b4e2a593dd8d18ebd711fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81758993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2219814d191a24c72b1054ecc5f1600df875adda53ee36add297c290f54aef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:41:51 GMT
ARG RELEASE
# Fri, 12 May 2023 09:41:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:41:52 GMT
ADD file:47682dd3869ca8e57ceb15f69a6ac7c9048d4d42c7a99a976e597cf072423c12 in / 
# Fri, 12 May 2023 09:41:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:35:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c67806d7e72dd941e600bad2eabe920a17ba1852b325b63900c819ffeae646fb`  
		Last Modified: Tue, 16 May 2023 01:01:48 GMT  
		Size: 26.7 MB (26715509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcb28dc5d7a6065807bdaa5cbff1c2a3066793dabe65b5f074ccd3a22365b7e`  
		Last Modified: Tue, 16 May 2023 01:37:06 GMT  
		Size: 9.3 MB (9341805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1444e209502691f92d74e355c2d738a6ccb71c9baf71e5eb601abbadf7a979c3`  
		Last Modified: Tue, 16 May 2023 01:37:20 GMT  
		Size: 45.7 MB (45701679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:670a252d4c2d3a1a9b9ec21eed6e7638346cc974993cf503a7d50f75e7c7f69d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71297778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bd71b5bdd3f1208c0976c7dd1e7c96189ca7caa0e4533806d4e23857bf9150`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:26:37 GMT
ARG RELEASE
# Fri, 12 May 2023 09:26:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:26:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:26:38 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:26:40 GMT
ADD file:c66513453620aaf35bbe377c693bac11a921cf12b7c0990cde7a0d5d113b93e0 in / 
# Fri, 12 May 2023 09:26:40 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:104619cc05a86891fa549978d70aed0cbcdf1e0a3f254eaa4f6c74fd7986232a`  
		Last Modified: Tue, 16 May 2023 01:34:52 GMT  
		Size: 22.3 MB (22308796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39260a49707ed839f4d9c80a95f22a42098cf4fc07351913c1839ed2bc5d627`  
		Last Modified: Tue, 16 May 2023 01:34:50 GMT  
		Size: 8.0 MB (7973770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c8762d1392b9b07677d512e282f400215bc071471212a4da5f403dfb3d2b2b`  
		Last Modified: Tue, 16 May 2023 01:35:07 GMT  
		Size: 41.0 MB (41015212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:26a76f2ac05dfd1034d9f4db4b81961bcb812f4d2a0a2417029420ffa5eb1044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75777358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129ba0eea7f82e6ce00f7f186220ac4bdb67ec3d5d57a421b34a60b367c5b66f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:31:18 GMT
ARG RELEASE
# Fri, 12 May 2023 09:31:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:31:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:31:18 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:31:23 GMT
ADD file:65c814904a00832cc69b4ef05c54d1cd3b570be2c12d8891a1472a73d6534cda in / 
# Fri, 12 May 2023 09:31:24 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:46:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:46:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d3196e9fda85b1ae1aa48fdd42a05894cf36dbbe8d2b8b75f46691b12cba022d`  
		Last Modified: Tue, 16 May 2023 01:26:21 GMT  
		Size: 23.7 MB (23740923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e3b3d51554b697c4f67290fccd0b73a47bc0dab65c7af6f1ae709dec1a42f4`  
		Last Modified: Tue, 16 May 2023 01:48:36 GMT  
		Size: 8.5 MB (8543977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30eaae04dac44c433a992ccb2f2a418da065c41261d4488a47590a01ece14a7d`  
		Last Modified: Tue, 16 May 2023 01:48:49 GMT  
		Size: 43.5 MB (43492458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b84f1720719266e0298594c94d50b0fc103568daec756c896adb08322baa58a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84313418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb65c0baee66d3f24b75fa9f4ec4f7e610500678f707e45bbf359a293c67354a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:14 GMT
ADD file:1f856710b4bf82e95a940e08c6167ef4775a430a38fd2fb575ad7743bacb39b6 in / 
# Tue, 30 May 2023 09:32:15 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 22:56:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 22:56:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:69f31bfb16537ef7adee6e0ba9f5ec28a58d51deecde164034a1b4a0e0c7d371`  
		Last Modified: Thu, 01 Jun 2023 23:00:08 GMT  
		Size: 27.2 MB (27170810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4928e6a80d2ff2c70a02c0eaeef3be857ef694a1da1ece8056a3ecda768a7bd2`  
		Last Modified: Thu, 01 Jun 2023 23:00:05 GMT  
		Size: 9.9 MB (9886063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ee804fd032478eb08e93d23f9f5cdd29859483e26421a40720c7b3089426a3`  
		Last Modified: Thu, 01 Jun 2023 23:00:28 GMT  
		Size: 47.3 MB (47256545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b7141721c1c36aeb08c52212453e0b366df30dca1d192fd1a6b820fc40567392
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94845665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9534ee764dbf3fb8374598c73c71754d969f8b59304886e3a1b922f695d1f00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:26:21 GMT
ARG RELEASE
# Fri, 12 May 2023 09:26:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:26:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:26:21 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:26:23 GMT
ADD file:362fa5164fb227e6f3d45a41742ca485fc50dde3cfdc3fdc1f9233011d3d1b84 in / 
# Fri, 12 May 2023 09:26:24 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 00:56:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 00:57:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab08883ad6ed65686edc81fb213d333beda55de0937170bd1f83540ca1d8f68f`  
		Last Modified: Tue, 16 May 2023 00:54:52 GMT  
		Size: 30.4 MB (30443542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8612663af4b782213cbb53b76c256a5a24aee62f19a60124bec464be1c91d4`  
		Last Modified: Tue, 16 May 2023 01:03:01 GMT  
		Size: 10.5 MB (10474415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c2c2f8054a6c2a3e88e6346c543ad5671c2424fd30cfc62c5a20f5807a3aca`  
		Last Modified: Tue, 16 May 2023 01:03:25 GMT  
		Size: 53.9 MB (53927708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e0f143746ec08a3de83bfd4cc45127f60cde71c3a0c351dc9073853776906afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79611765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48d35492d41f963807ea390ed16c15e2d0a999b60e12b13c3fbde16b58c6e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:26:12 GMT
ARG RELEASE
# Fri, 12 May 2023 09:26:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:26:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:26:13 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:26:14 GMT
ADD file:8abaf7bef475e944e369ee2369d14001ea58594579438de5aa0e2fa72e805c72 in / 
# Fri, 12 May 2023 09:26:14 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:11:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5490589b1a9dd4773f02a935037b1960843ae0c35ff2284a0209a8d6d948a95`  
		Last Modified: Tue, 16 May 2023 01:16:19 GMT  
		Size: 25.4 MB (25372959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bac593a1156dc49dae6ac86a45fc34982b24751af006b77e6876a5c04fdd713`  
		Last Modified: Tue, 16 May 2023 01:16:17 GMT  
		Size: 9.0 MB (8982576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e6787d7045a27db04a439e0e0dc9497702567502669dfe4452c953601bd6f8`  
		Last Modified: Tue, 16 May 2023 01:16:33 GMT  
		Size: 45.3 MB (45256230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
