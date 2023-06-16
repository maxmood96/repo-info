## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:618ed9c72d41aac38dd290fe26868aecdaae70f4ca7aebc9d25619b9994f0066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4f007eb982be85b8ca4b7dddb23bb3acdf51c1ab865d86cb3a99f9fbdbea91de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85694752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2193070b01a96fadfa62cb44f611ff3c057a26cd32a0b2a39d3b8f161b5a3a43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 09:16:59 GMT
ARG RELEASE
# Tue, 23 May 2023 09:16:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 09:17:01 GMT
ADD file:6591237a72178b71d79f687b816ad23237fbef0bc3ec42332369d9e7bdaa04e4 in / 
# Tue, 23 May 2023 09:17:01 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:43:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e4ea5938a80fb79461962ff5189dfe6a9611db20e7fd777d48e9c1fb890dd7d`  
		Last Modified: Fri, 02 Jun 2023 00:50:42 GMT  
		Size: 27.6 MB (27604778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c71826d6ef94eb72f39ead11e9bf5bffebf6621de6a623a7219ccbe084e7a9`  
		Last Modified: Fri, 02 Jun 2023 00:50:40 GMT  
		Size: 13.7 MB (13743419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b272b87751d403529d61b4fa7a58440e4c95528eb9ff983882453e8e7d2591`  
		Last Modified: Fri, 02 Jun 2023 00:50:57 GMT  
		Size: 44.3 MB (44346555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5a6012c64abe5a1e4977712e462e6802d4c5e7a02f2030a15e71b72ff3dfe57a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86748441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23973e09ff69a4949c38d23ac559b76967b561c2e71a9c4d1998f800fc603a88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:49:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:50:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca5128fe76949cc104af7f40ce0f7213fe093079077d47dd525fa0189090c57e`  
		Last Modified: Fri, 16 Jun 2023 00:59:51 GMT  
		Size: 25.4 MB (25432780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8ca764d56bdf14c46fabd5c4e2e988ce166d01c8c0631d7c345802ace7bf1`  
		Last Modified: Fri, 16 Jun 2023 00:59:50 GMT  
		Size: 12.7 MB (12662932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b3e8b607724476a55e2e23faa2859f1e37c17323d12df2f9b87de3745b98e3`  
		Last Modified: Fri, 16 Jun 2023 01:00:07 GMT  
		Size: 48.7 MB (48652729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e23f7ddee582c489850584729dc784bc6bfa06266589e0477e9db39d6069c4e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84543069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92f77396201196a947672068fa0b228fce4cfd218400aa94d95ec8e5ddf09b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:45 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:47 GMT
ADD file:b2902a85ba60d642b00f2d7d7e4f56825749dca527e2d8d5e64d854c76ed28f0 in / 
# Tue, 23 May 2023 08:33:47 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:57:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:799351a2e050dcbccac2616755ae9631d97278ecebbd4db013e40b3a849439c5`  
		Last Modified: Fri, 02 Jun 2023 00:05:52 GMT  
		Size: 27.0 MB (27017966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f53223904f9116e3fca0e8c45abe0ddd4a8c43584afe7ad09b9406e2d26a91`  
		Last Modified: Fri, 02 Jun 2023 00:05:49 GMT  
		Size: 13.3 MB (13331051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8e19cbae0e39a2642e58e9a773ece1aac1b0cac4eb9eec6c8fd81b765ad2dd`  
		Last Modified: Fri, 02 Jun 2023 00:06:05 GMT  
		Size: 44.2 MB (44194052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f8e4e5d3de0c2d936e3cbb4b9dba0c0b38c3b069c6f9ebb5b38f09d98f48280b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96881709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94999d868ab69a94679f2c0667a9007f374e14e97012df23ae637bb59ce7ea6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:36:49 GMT
ARG RELEASE
# Tue, 23 May 2023 08:36:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:36:52 GMT
ADD file:d76035fa745d219f333adeb90e6eedc3b563dca64aa80c2fbe88d7389ba798d2 in / 
# Tue, 23 May 2023 08:36:53 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:07:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:08:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:949f734ad643dc041d0099be4f14b5d487e88ee4a4715547d536c0fb34f3d2a5`  
		Last Modified: Fri, 02 Jun 2023 00:24:59 GMT  
		Size: 32.0 MB (31997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94c6acbf105653fae1ce0dd770ebaecddb43ed456d1efec703ab88302a258e5`  
		Last Modified: Fri, 02 Jun 2023 00:24:57 GMT  
		Size: 15.8 MB (15840641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2543924bc730178b71560bbf215eab51af39beb08abc751cf0ceb20febacfa11`  
		Last Modified: Fri, 02 Jun 2023 00:25:21 GMT  
		Size: 49.0 MB (49043911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21b84104632a19001f156bfe11cb32433c0b7dcd573221d5703508844a3c8591
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84463563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bd0326ad6a93dcaf2ea15084e7b90c399636f79c5a83253203ef2c4f01299d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:34:39 GMT
ARG RELEASE
# Tue, 23 May 2023 08:34:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:34:41 GMT
ADD file:390d5b6c76bd6ae4f2901362d9a308f7dc4fa9a83574ec3952e867bc951c1552 in / 
# Tue, 23 May 2023 08:34:41 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd80ecb7763a9e3fbf3b7c2b815d337acc04e6d1a42898eee903ca05160f9419`  
		Last Modified: Thu, 01 Jun 2023 23:19:54 GMT  
		Size: 26.2 MB (26236512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05916a9cc39edfb88d065692b72105e6d80b81387a04f196cce1b55eabc17c66`  
		Last Modified: Thu, 01 Jun 2023 23:19:53 GMT  
		Size: 14.0 MB (14003969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbda1a8e864725727f7e49613e295b1cab05586208b442e983a8de1d47289016`  
		Last Modified: Thu, 01 Jun 2023 23:20:06 GMT  
		Size: 44.2 MB (44223082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
