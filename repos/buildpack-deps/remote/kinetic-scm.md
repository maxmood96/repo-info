## `buildpack-deps:kinetic-scm`

```console
$ docker pull buildpack-deps@sha256:6ca440a4a439dc6f8de6e677eb8d0fbaed5beeab41046c22b38835d8e28d0d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d52ddd72ddd4f630e64370ad14d0ec6b99705784fc76f396c2d3d67230db3403
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81504021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec8c6e4d643fed5a6197bd272d12574893b6727b71d0bddc0526d40019fb457`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:07 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:23:09 GMT
ADD file:50094673f74cf3945ac21e23bb84d41d3516bc1ac90ebf7f17379288c33c17b2 in / 
# Wed, 28 Jun 2023 08:23:09 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 03:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:44:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4ae0f456d5b5ed53c0d0f67cd1948207060810837f2b15dcdf5bd97bbceb300`  
		Last Modified: Tue, 04 Jul 2023 03:56:47 GMT  
		Size: 27.5 MB (27488903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f7fd2e9f809d0b31bf96fde0b09fb68493e5499b9a4dae5f3dfc0a0ed0b7ce`  
		Last Modified: Tue, 04 Jul 2023 03:56:46 GMT  
		Size: 14.2 MB (14189206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e60069d839c80c438523487b52eb9073ef4a8fd32af5b8a6dfe8480792c8a57`  
		Last Modified: Tue, 04 Jul 2023 03:57:02 GMT  
		Size: 39.8 MB (39825912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:44b7926bef25e86fda0ce933db0a51672dd4b6569f40fbde5413b85c40259d7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81993193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1888d5faa20899d778ded8b8bc5a0d939c3c81a8d6ffeffa5669bf0f8dc8a9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:50:23 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:50:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:50:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:50:23 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:50:29 GMT
ADD file:1c3ce20a4b19d1c7779aa47e9799d2887ac4d142bb495eb0bdca08ff1c8fd106 in / 
# Wed, 28 Jun 2023 08:50:30 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:09:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:09:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b2a8550df843bc39f9334e8b8d8524b0e0abe390674577c839e53aa1c6afb06`  
		Last Modified: Tue, 04 Jul 2023 06:24:17 GMT  
		Size: 25.9 MB (25912764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eef66710f99af0d044d772f07b2eaf0c9da9559b1b10f9da05b104e86fb12a7`  
		Last Modified: Tue, 04 Jul 2023 06:24:15 GMT  
		Size: 13.1 MB (13141364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f28d29b0c8e6083c797c1ed79183346245421c696c0b8365d1b4027561dc13e`  
		Last Modified: Tue, 04 Jul 2023 06:24:34 GMT  
		Size: 42.9 MB (42939065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d82da2a7c889be494f08719c2be0bae60e0130d8f57987e9dbbefe8771bc942f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80095209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eaa9e6f7cd4097cd50bf0de7c32b8d39d1c5d8ac59cf278e3defea8e03a703`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:16:50 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:16:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:16:58 GMT
ADD file:a41ad4058e77a6f1ee9800af03cf13403d5d844e876246ba55c4ceb2106b6d5f in / 
# Wed, 28 Jun 2023 09:16:59 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:11:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c5528eed9908e3645e0eff6666ba300d135b6ff9801f5ae1cc49bb06a3f29fcf`  
		Last Modified: Tue, 04 Jul 2023 06:25:40 GMT  
		Size: 26.7 MB (26730941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8785a3c2b399ffc53927bd8e5eea56d2819ea053d0d78910ae32f88d2f9ec680`  
		Last Modified: Tue, 04 Jul 2023 06:25:37 GMT  
		Size: 13.7 MB (13727615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af381f44d3219c7eab50c1af5c7bf36233fa1a694569f8a29e1be2e7d55cd37`  
		Last Modified: Tue, 04 Jul 2023 06:25:53 GMT  
		Size: 39.6 MB (39636653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:264fc69c8de3193a7191aae5bb3f4c3db4fbf1a9f0e72d801c70971713aadbda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92568101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6367bde1dbdeeadc100e3b50d95455d079ffc7c8f892d24e31742464e7e00931`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:04:09 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:04:12 GMT
ADD file:8c5e727842a7ff4d34b93a1ee45f14532c9b03594ad53400240e6f0f4b99b390 in / 
# Wed, 28 Jun 2023 09:04:12 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c4c2a73576db8e1d5b385d67fe412db5e6cd146167f6c5fa6153b87f17abfc3d`  
		Last Modified: Tue, 04 Jul 2023 04:44:10 GMT  
		Size: 32.1 MB (32102426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297facc34b9d65726d36999c1b9378836014f1dbb15725b2be4359b50bec9d21`  
		Last Modified: Tue, 04 Jul 2023 04:44:07 GMT  
		Size: 16.2 MB (16234063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb9fc38b5a1da1252223c33aa1381def6fb94284f39b6c1d6025d92bf99478`  
		Last Modified: Tue, 04 Jul 2023 04:44:34 GMT  
		Size: 44.2 MB (44231612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:749616a3d80ce076f174efe52ab324d25a6fb91799a0be44c3b5ec95d468e9df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80057057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e27248efe9b740d475c4c4dce3899539f672e413e71005bf1c2b8ce39fe9eb0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:10:49 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:10:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:10:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:10:49 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:10:51 GMT
ADD file:2390e4c5ac4f862cf5fb266c70962a01f271fa692b74af886f18911482025825 in / 
# Mon, 05 Jun 2023 17:10:51 GMT
CMD ["/bin/bash"]
# Sat, 17 Jun 2023 09:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Jun 2023 09:50:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45d37589c642f2585803ed2ba24d2b897920c885c7a913bb399e12a2410d5503`  
		Last Modified: Sat, 17 Jun 2023 10:01:25 GMT  
		Size: 26.0 MB (26034488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10ce8336984e795efd05d14a13611a92ef77b199d749859036bd37fbbf18040`  
		Last Modified: Sat, 17 Jun 2023 10:01:24 GMT  
		Size: 14.3 MB (14344562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f89ec5257613dfb7e6ac3731cf008ae93397126d7d27b80d7d9e63428331cd`  
		Last Modified: Sat, 17 Jun 2023 10:01:38 GMT  
		Size: 39.7 MB (39678007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
