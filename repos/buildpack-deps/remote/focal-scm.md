## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:0b1f4819bc19d2a7dcd6f97819a64535e012ee8b22fefe0e4b1436508ba06096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:698f4f88683377c7cf50697f320acb706f221f443170f63266179f5609f678ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100629710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68639948b98bf3811760171434939a474a1e9c4655266606929d260fa4b940d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:23:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf9230833027caee5149b71822c6d0e2d47aaa0fd62e1d87413060918e0835b`  
		Last Modified: Tue, 02 May 2023 23:42:40 GMT  
		Size: 11.1 MB (11132922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3ecfa6d2583eedca622bd71b015b74c55750afbbffb22ffbaefd2aa96865eb`  
		Last Modified: Tue, 02 May 2023 23:42:57 GMT  
		Size: 60.9 MB (60918225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9aeda7f50d0358cf65750d317f5698dc2850aa9cacef69db1bced2b073625c21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90014376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1b40546bb31e651ded1a12f8965865aba2f9ae18b814eaaf42d38f960e9866`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:19:26 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:19:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:19:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:19:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:19:31 GMT
ADD file:114d6f55f8c1c4ec7f7d2ba3c803116a188eece1d1b6dbb3bb40c11082194234 in / 
# Mon, 05 Jun 2023 17:19:31 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:36:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d97abfcf215d35e8a846b390350fea9f455676b41221360fe8782163a1c46bb`  
		Last Modified: Thu, 15 Jun 2023 03:47:54 GMT  
		Size: 24.6 MB (24589116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfa3e878b28f52b3f5baf56536bf558319d9ba6f891e7b4538b19aa25b04c83`  
		Last Modified: Fri, 16 Jun 2023 00:57:07 GMT  
		Size: 9.6 MB (9599122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e6a97b22f3d20c527ea6848d6ac5240c8244afcdfb72f4d25159f61fb48b40`  
		Last Modified: Fri, 16 Jun 2023 00:57:25 GMT  
		Size: 55.8 MB (55826138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9fc3849335445c509099e2edde9290bd49d33d6d0b29e5aa8953c3f878b160a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99192457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1d4fae746e7e7a58d1dfb18b30bd8e7647a88d7f15b3ffb70449d2e85ad52b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:51:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:52:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19555cdcc8d7a940da1d4ed225123c187d6698d19d09be9ccd924bfd48a2d4b`  
		Last Modified: Wed, 03 May 2023 00:14:39 GMT  
		Size: 11.0 MB (10984596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81fab6c64581762d2a9ebff845cc8b7c02741c50064ea02846a914e67ea244`  
		Last Modified: Wed, 03 May 2023 00:14:55 GMT  
		Size: 61.0 MB (61011465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d110226a5bcd736eb42d03d5a3f0b61d4ae52e0f3c32bc046358d22050c3b301
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115881656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86caf7ebf93f8a2cdcc71d11c10822862479099ea2ff71bedecca9f72fd393f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:43:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd267849179c50e36c7bc111bbffbfbb6795cfa3d55e9b77e19e34ca34121b9c`  
		Last Modified: Wed, 03 May 2023 00:17:37 GMT  
		Size: 12.9 MB (12949724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b128fedf49b76b0c1569492608c62ec5c8db31a1f64289e314a63d23788fe954`  
		Last Modified: Wed, 03 May 2023 00:18:05 GMT  
		Size: 69.6 MB (69630952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cfcdb8fa619680063354c66ca5a5392f4f88c5d9610e4f885aa5fd73c7bc464c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98020918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5d06d35eb3d9888bedca9fb4a63ff62e7b5de29e51f3cc8be5c9de9cec88be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 03:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:17:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448f2e010a52f914aaf817d2504cef91c342cff6be87dd877c7ba39296277353`  
		Last Modified: Wed, 03 May 2023 03:36:13 GMT  
		Size: 10.7 MB (10691882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc0e33219b4fa365453005d655db0337ac98461d451db2bf1468fd56e5b216`  
		Last Modified: Wed, 03 May 2023 03:36:27 GMT  
		Size: 60.3 MB (60312666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
