## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:fafd6ef29ba54523d8767c7b0ddd6c538581b43518cb9f2adde54c6fe256df71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4f05fe4621946ecbd95f3f060b43b11e33c26d171edd465a0578f133a34b06f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85636697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b1ef3420e0f56df66ad3aa3f4c8e50a25ffab336ac5225dbe7cd55fbb3c879`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 12:44:41 GMT
ARG RELEASE
# Tue, 09 May 2023 12:44:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 12:44:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 12:44:42 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 12:44:44 GMT
ADD file:f074265119093d25dbd3022b9335bcff83e7bd893a43de3f4c62e7b9f86f3180 in / 
# Tue, 09 May 2023 12:44:44 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:37:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f0f0a5354c0ae208576c462d933b6dd9937ba3a0e0109fe6aaf52332686d5c4c`  
		Last Modified: Wed, 17 May 2023 00:43:35 GMT  
		Size: 27.6 MB (27616500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3f8ccb1549a815e890ec3e685f1dc0553f12021c3f3a0c180f4b7205baeca4`  
		Last Modified: Wed, 17 May 2023 00:43:33 GMT  
		Size: 13.8 MB (13760620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bcb3327d8b3dd236d5bf1af06e0b53ed8fc0b67b6fb76bfbc30bf3181b5229`  
		Last Modified: Wed, 17 May 2023 00:43:51 GMT  
		Size: 44.3 MB (44259577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e01202bfa398b440287a7ddb34cdb1a3b2534b61b05544efecb25640a3f50beb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86410586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b28c0542f8a0a467885d1d35ad02bd7c1bba1e6cce76cd370e295c25089724`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 12:44:03 GMT
ARG RELEASE
# Tue, 09 May 2023 12:44:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 12:44:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 12:44:04 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 12:44:06 GMT
ADD file:db8559cdcf696ac1fdef17e2d7eabaef48d874580294f6af72e95bae947fe358 in / 
# Tue, 09 May 2023 12:44:06 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:20:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:20:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40a8bf5385e89692116e9cb0b4825cde587032e63bda722363b1e26492f6612e`  
		Last Modified: Wed, 17 May 2023 00:27:52 GMT  
		Size: 25.4 MB (25445595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01204a82cb455443751eaf82e1bc6909d3c718919dfdc9835bf83e8e8279d5ef`  
		Last Modified: Wed, 17 May 2023 00:27:48 GMT  
		Size: 12.7 MB (12675867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea226e2025d1b7a7f538848d7902f6c862eae0e2146095743300de693a05d8b0`  
		Last Modified: Wed, 17 May 2023 00:28:12 GMT  
		Size: 48.3 MB (48289124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:703b9d73d29dbe60355d9ecf0fe6314451ab05477344d7fe427c438d1fb175d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84439900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29ed0148a16f228f641cf237dcc5523e4b7cdaa95a7dd7ce6134780a0628a31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 12:45:45 GMT
ARG RELEASE
# Tue, 09 May 2023 12:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 12:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 12:45:45 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 12:45:53 GMT
ADD file:87293581d53f522106a37eee2d3056cd4d9bdbb4a58077389c817bd655a4e0c7 in / 
# Tue, 09 May 2023 12:45:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:54:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e685e76ac424b804c8b8208c603584b34300a955516eaff83d30f060189f522b`  
		Last Modified: Tue, 16 May 2023 23:59:49 GMT  
		Size: 27.0 MB (27026748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccd2979a9c21a4b382153460cb77e2f6d383b4c4cb5cdeb37baa35c84e174a1`  
		Last Modified: Tue, 16 May 2023 23:59:46 GMT  
		Size: 13.4 MB (13350711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342807f1db024cabeca1aa775473201ce240f01d11faabb59c89f443a7bc8cad`  
		Last Modified: Wed, 17 May 2023 00:00:03 GMT  
		Size: 44.1 MB (44062441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:085035afd162f9e54e0e22b3c990da36b159310b1f9b97298734be10df6f9a0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96792724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79a39116f27f124d688e45c59da736cd6747792cd7251e4262297b114be28c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 12:44:00 GMT
ARG RELEASE
# Tue, 09 May 2023 12:44:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 12:44:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 12:44:00 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 12:44:03 GMT
ADD file:d42dac32e11311d9b5e412834823455c0173f98c6a52bbb537a30dffb3bc872f in / 
# Tue, 09 May 2023 12:44:03 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:43:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fa2defe9dba792ccace369ff4376838b0ce6d5a66b5f5203aa26761e8d1494e0`  
		Last Modified: Wed, 17 May 2023 00:54:29 GMT  
		Size: 32.0 MB (32008882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ccf43574a204fb203da7c5786f2d89752ab4c468f685736027513b4113c7cf`  
		Last Modified: Wed, 17 May 2023 00:54:22 GMT  
		Size: 15.9 MB (15853739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e7c3553a23ef622a22c0162c9dd8cf6187b2dbeab9d60ba926cd4766837911`  
		Last Modified: Wed, 17 May 2023 00:54:52 GMT  
		Size: 48.9 MB (48930103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21a95cdd7cbd011e112f406d36a23f51265a389f8f0b04923caee0cf7216dcce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84351533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6b3b9deabe2fa382fac07948bb15670db21d8aef8e165bb8b017a3fbac4983`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 13:09:19 GMT
ARG RELEASE
# Tue, 09 May 2023 13:09:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 13:09:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 13:09:19 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 13:09:21 GMT
ADD file:a5ed2ab846477e26003abb09795ef405e1d96bec9be1a3cb0b258dd5aa83f075 in / 
# Tue, 09 May 2023 13:09:21 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:52:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e21501268ba0e8cdc7e0134b231643691b6d4648511a6bbed295eeca807810d8`  
		Last Modified: Tue, 16 May 2023 23:58:10 GMT  
		Size: 26.2 MB (26239447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b45801daded85936f7c762c0148a3d71e35c237bfe96ba49811f0964c16cb9`  
		Last Modified: Tue, 16 May 2023 23:58:08 GMT  
		Size: 14.0 MB (14018228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1711be48a0a429b31d94131f11f34c0b5f5eb3de15640bbda8ad0c25bba80a0`  
		Last Modified: Tue, 16 May 2023 23:58:21 GMT  
		Size: 44.1 MB (44093858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
