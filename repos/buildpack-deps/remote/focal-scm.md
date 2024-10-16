## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:505fc4c7c1a8ab80e7d1a4b3192784aed4950cc69ba92cdf5c34084438e809f1
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
$ docker pull buildpack-deps@sha256:24fb1d94cdeb62452080ea88d57009d977d0ebc6145bef70b355217f0c0f3fe7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100657473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaec521d79a736d2c908b76567cb34fe6800cda4cf11dd3425c35d5e57a60824`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd558caa256cf95484f8e02652eae57ccd55e76f1d0013d3068ed05810fdf6e`  
		Last Modified: Wed, 02 Oct 2024 02:10:52 GMT  
		Size: 11.1 MB (11148997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9411f4debc2af1b53b390cebb61b5125cc06e081e824a5825224cc682c2bf773`  
		Last Modified: Wed, 02 Oct 2024 02:11:09 GMT  
		Size: 60.9 MB (60924590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c1a6e7fff25cd5cd4577d9b2916182b135715d9a80b65798bd9f6957a61933e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90105028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2c2ac3150f534f92f33ffa953a9903dc97fc9d4ba861bf839905461129eb86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8360546e6d28ec60104c18634d12f2178926b9e6c3aed4d2bff7b0c7062e0858`  
		Last Modified: Wed, 18 Sep 2024 22:25:20 GMT  
		Size: 24.6 MB (24600195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32d29ba7f69bfe4da5af94ad45d2f03c338ea6e70a2bafdec2e7eacc4168233`  
		Last Modified: Wed, 02 Oct 2024 01:42:48 GMT  
		Size: 9.6 MB (9621707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60e2872eabcd665fccca4b65322b8780ad6b271f98a487b9d013700d8c5f24`  
		Last Modified: Wed, 02 Oct 2024 01:43:08 GMT  
		Size: 55.9 MB (55883126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:27376f7d6da57e2d59d855f0c64d760261b3582adb037e2587288b0fb5544370
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99260509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3d9e73afca1925b94ce7e6fd49da77bc0b0c88092d11eb22c98ed3a65c5436`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1923e7b81f85e94df308df81e9c261152ee5ca8605cb2b79eebe8714847d8bc7`  
		Last Modified: Wed, 02 Oct 2024 01:17:18 GMT  
		Size: 11.0 MB (10993171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670a3422be6c3e543f9ce6d7faec576205d847616531df1aa7e2a7eb4af90ae`  
		Last Modified: Wed, 02 Oct 2024 01:17:37 GMT  
		Size: 61.1 MB (61063346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7af077cdf974af9fe86ec9e2172292e1c3e38ab8fa006852a21ff906b43d08fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115942647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16138b3caaffcda0cd765a593a804d16d4abeae15bc694284c03ac99ba2e3dea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Oct 2024 01:39:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d722867b7a3e593d9beb32c0893b52b8af91fdc3900efd1974a57e6c8800771`  
		Last Modified: Wed, 02 Oct 2024 01:54:29 GMT  
		Size: 13.0 MB (12963170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade1a5274d6f1d0318337f54ba1338a12318fa208dc455dd515fa9ef53b0e5a`  
		Last Modified: Wed, 02 Oct 2024 01:54:55 GMT  
		Size: 69.7 MB (69663914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:78631683c7e021c9b83e5f6c59b82a784ec2ad419bfd6b2f85eea7721ca50356
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98072568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ea0f7d5580b3b0060c2bce75d80338579b73ccb93db238a866f0abf88f7d34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:09:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:527495b21ae4efd3ff5dea679dc71a1631f2a861f8be8f838ff10c5176246b80`  
		Last Modified: Wed, 16 Oct 2024 01:16:56 GMT  
		Size: 27.0 MB (27012438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e68a2830833de9a843a3ee8d2677504bcdad17830e1e5e98506e72e7b73dfd7`  
		Last Modified: Wed, 16 Oct 2024 01:16:53 GMT  
		Size: 10.7 MB (10705495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8f6200608896e11eb9c555f60321de8024fd186eda924fac7d707c8635deb6`  
		Last Modified: Wed, 16 Oct 2024 01:17:10 GMT  
		Size: 60.4 MB (60354635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
