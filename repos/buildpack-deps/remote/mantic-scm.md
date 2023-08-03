## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:fcad3062d49049c1cd6b7aaa78ef9bb6aa7130725d30cd26cbc66f1f8d7852b0
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
$ docker pull buildpack-deps@sha256:85d72857fea95aeb6d112513da095e1878f6e1efa45f440f9dcdee9d9a0b5370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86321874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7b8afe3427bf251dbae8dba5b9d858cdb087aeed3dc518427671aa5aea9ea4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:50:42 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:50:44 GMT
ADD file:592c8f21973a80f096ca38aaf5ef478d80f666517a169bc638ebb325f5ae07f4 in / 
# Wed, 12 Jul 2023 04:50:44 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jul 2023 01:45:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c57e6f7e53eccd34261640d6f245ad38a4ff7cc54ead279536b568d836363ae4`  
		Last Modified: Tue, 18 Jul 2023 01:49:46 GMT  
		Size: 27.8 MB (27758391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70262639a4fd505c867f716c40dd85135752950cc1aa365725b9e2967d66175a`  
		Last Modified: Tue, 18 Jul 2023 01:49:45 GMT  
		Size: 13.8 MB (13781000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade5aed8da7a4eb9b7d6f71f11a953d3491588e96cb6cd244876de5a69a96cea`  
		Last Modified: Tue, 18 Jul 2023 01:50:01 GMT  
		Size: 44.8 MB (44782483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3b16df0cdce33f0ee6279409ac982bdb50248ac00be43888721544867e49c77c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86933441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da3ba7664b82a047c70a8e69802637f613f60612974e0f52c505163dcdb1be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:54:17 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:54:20 GMT
ADD file:6f71de5b8467fdcd7bcf88fbae117a520f903a91b00a674bdf8d44b14141f0d6 in / 
# Wed, 12 Jul 2023 04:54:20 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 04:39:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jul 2023 04:40:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d27378af227ba4634a3837d7cb24660c6d297228e3b3a59b569c67e86c1b702`  
		Last Modified: Tue, 18 Jul 2023 04:44:33 GMT  
		Size: 25.3 MB (25310196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c20ac942533d1efa51f9b7223514a74aa29ec7a0272a22f2f548636534fd3f`  
		Last Modified: Tue, 18 Jul 2023 04:44:32 GMT  
		Size: 12.7 MB (12697617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5550cb2b09d3bf2b56d01eee2a5d36ef7263a4f3b0d35f84ebe938e6f64ab689`  
		Last Modified: Tue, 18 Jul 2023 04:44:49 GMT  
		Size: 48.9 MB (48925628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9122b1edbd4adc38ccc58f3920ad46da438065404b2c2b313e8dad8197d088e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85213455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce76a6c7918f1651f24f52ff3c5b7d55274fb11ed64e1e65df322793c82ddc01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:33:27 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:33:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:33:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:33:27 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:33:30 GMT
ADD file:17fe422cc794db64e2ba81827bc4b023be475037fbb2287e9a8f9b3188870856 in / 
# Tue, 01 Aug 2023 05:33:31 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:44:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1a3c0e88f08f7d351cfc817115213c0d385cf7f0ed6155cc04dc1182729b19f7`  
		Last Modified: Thu, 03 Aug 2023 00:51:46 GMT  
		Size: 27.2 MB (27213589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c0d4e14f14d4983ed44a97aef21f464ab3ab57579e47f62f3cb6f2a4561fdf`  
		Last Modified: Thu, 03 Aug 2023 00:51:43 GMT  
		Size: 13.4 MB (13368973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc46dbe7684b7b3276598eb977471567780b9839150b5c5b707c64a73a4bbbb6`  
		Last Modified: Thu, 03 Aug 2023 00:52:01 GMT  
		Size: 44.6 MB (44630893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5427d53e2a0f36be11ddee624b8c2282efb28ea974220e842386fef4566bb3ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97390756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490ac353d73761f55f94aaa4b8e908f4e3c1ecdff0aeef98c7eb21967229e66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:53:28 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:53:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:53:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:53:28 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:53:31 GMT
ADD file:7028e8b5bb04424a3fa537fa5b5a311cfcaf1c8b6f321b414b40ee0388d0f9e0 in / 
# Wed, 12 Jul 2023 04:53:31 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:52:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jul 2023 01:54:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaefff58e8d715237ca48dbc24624ab97d73780134b6abfa9397a3fb107c7847`  
		Last Modified: Tue, 18 Jul 2023 02:02:03 GMT  
		Size: 32.0 MB (31995451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3142716ff35072c411419b141a83ce524bc1af91e86195277f4ca49673988b19`  
		Last Modified: Tue, 18 Jul 2023 02:01:59 GMT  
		Size: 15.9 MB (15880046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5986d60cc2d030634cd4d91824fd3926b4c50f5ff1bed4d038671c930e6dc5`  
		Last Modified: Tue, 18 Jul 2023 02:02:28 GMT  
		Size: 49.5 MB (49515259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e2be1e684ed36c83a4386aed999d61829b37672df08deb3e2c9c27db3efef6da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85405385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b3dac9f5150bdd8c702d3cad0ab14d4105892e87f5443890e8b335b1b11217`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:32:48 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:32:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:32:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:32:48 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:32:50 GMT
ADD file:dd263eea5d15c08fe1aa830f7313ad188951ffe22caabbf664edfa2459c63b99 in / 
# Tue, 01 Aug 2023 05:32:50 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:17:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da7f02973684568dd47cf916af8e79783f8ec0ce768358ad7dd50a79e2090c53`  
		Last Modified: Thu, 03 Aug 2023 00:22:47 GMT  
		Size: 26.5 MB (26537706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ca0e17cab3bf50e237aea2fbaac414404d2f0cef2fc329f9eaa94169a777cd`  
		Last Modified: Thu, 03 Aug 2023 00:22:45 GMT  
		Size: 14.1 MB (14052687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6814bfc1e50d3e20bf4c3b19a6345b45a53e9774fd7596694ae808bbf81bb66`  
		Last Modified: Thu, 03 Aug 2023 00:23:01 GMT  
		Size: 44.8 MB (44814992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
