## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:321843ed5fb07473e46c62dd444a835a204d5bfd5f49bbcfc6b078db776813e0
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
$ docker pull buildpack-deps@sha256:405d376e0a44215dd53d9e4cea3ff098d03cae9e0aeeb846816f17d396321b18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83062814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3aba9e6064055dae56a062bcb092f50cffe5887b49242fdff98a4ea0eb3aa4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:04:48 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:04:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:04:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:04:49 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:04:50 GMT
ADD file:492ae1940ef5a9a4d7af92b9120b5b7c7d3bfd8107ce94d28eab844ace024981 in / 
# Wed, 11 Oct 2023 18:04:50 GMT
CMD ["/bin/bash"]
# Wed, 15 Nov 2023 05:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 05:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e92ecfee06656d1e7ef085e24769afe12ea1e14f3acdbdaf9d5cb922da5d97b`  
		Last Modified: Sat, 14 Oct 2023 00:22:39 GMT  
		Size: 28.1 MB (28067323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a6e6c1f13a01a9a83ddb22794e5e9998c28232b9695a11941b9c2fad7dfcc9`  
		Last Modified: Wed, 15 Nov 2023 05:19:05 GMT  
		Size: 9.9 MB (9907184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fdbffee3006b2f392267c0bb2881b445fa2d9a6a932b40496bf246d26ed245`  
		Last Modified: Wed, 15 Nov 2023 05:19:22 GMT  
		Size: 45.1 MB (45088307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:afca6c528e9a02dffda09b471ae45eb3c1cd24ff62f025ec89877622c62fca52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84386409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfd5fac42f464b6ae54e8ee27cba67ca6befadd81810a15993572f7fbd736e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
# Wed, 15 Nov 2023 02:04:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 02:05:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:917b6666fb3ef51da1fc4435b7ebc2e973f8582d1321861d37d40dd0864b8927`  
		Last Modified: Wed, 15 Nov 2023 02:12:00 GMT  
		Size: 26.0 MB (26018438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179cd7cba3839185a2e0560fddb5800f6454b72d5acf3d485458ee26f6fef69f`  
		Last Modified: Wed, 15 Nov 2023 02:11:56 GMT  
		Size: 9.1 MB (9144906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43664e3e871d40780214b000e38e04e3e840e99201a63699c325b0f02b0e5c`  
		Last Modified: Wed, 15 Nov 2023 02:12:19 GMT  
		Size: 49.2 MB (49223065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b90f855ca6f36a58ffa93d51518b716154ce46f2501c052255a4ca69820f5f40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85341235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1353821bcafbdc837c170ac7e68154a2784c2c9be1397d618829b032d0afd42a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 05:06:27 GMT
ARG RELEASE
# Tue, 26 Sep 2023 05:06:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 05:06:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 05:06:27 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 05:06:30 GMT
ADD file:0dbbd4de9483bc32897d525742b94aa13ebd3a6aac7f1844d94d7f4536b2bfb8 in / 
# Tue, 26 Sep 2023 05:06:30 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:17:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:18:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4259d3adacfee572bed7acadc8e4af2cf679658d229fc94eb25abeb6d662693a`  
		Last Modified: Tue, 03 Oct 2023 06:23:31 GMT  
		Size: 27.3 MB (27315811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e515aa13e7ac1bba03883084849baef28268d175299a636c354b0e7558af88`  
		Last Modified: Tue, 03 Oct 2023 06:23:28 GMT  
		Size: 13.4 MB (13394041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a515dbb7fdd56d447a83b9c10d1e2ec2fb52e85daf470e09424283d14b5908`  
		Last Modified: Tue, 03 Oct 2023 06:23:44 GMT  
		Size: 44.6 MB (44631383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:710b61b098eb5d89e1e90686bd2c18ab1114706836bec26a133f94735ca05450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93822307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e385101b300162a4d39d603be56508551348b1b4e836cf511396429cdcd345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:06:00 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:06:03 GMT
ADD file:a18be8add7eb60493b13d2aac8d624230297bd15be033756795582dc07cb04bb in / 
# Wed, 11 Oct 2023 18:06:03 GMT
CMD ["/bin/bash"]
# Wed, 15 Nov 2023 02:22:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 02:23:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cffa8c08adf985954e82a5191220c2cac943e97ffd91acc2baa5d2cf0f8d4f44`  
		Last Modified: Wed, 15 Nov 2023 02:29:45 GMT  
		Size: 32.3 MB (32331370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5791ffbc3c4fdf8ff7e22c644078ce798cd8033f9d2e244eca8aec0a44ac5ce7`  
		Last Modified: Wed, 15 Nov 2023 02:29:40 GMT  
		Size: 11.6 MB (11573378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6331f990f21c8548212ac022cb9047ae9a7b4ac314bf49338f47926ca887eb14`  
		Last Modified: Wed, 15 Nov 2023 02:30:03 GMT  
		Size: 49.9 MB (49917559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a91a88d92cebe1e06032a2e91eca9eed7764f96574bf8209a0e634b723902068
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82887049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f810d9541dc377d4af2da31b65e5188e4419926498729a02895e8664cdb624`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:03:34 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:03:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:03:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:03:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:03:36 GMT
ADD file:8ceb0028af8276b03b6c88b19445f30165a41791919c756e1434da6ded4387db in / 
# Wed, 11 Oct 2023 18:03:36 GMT
CMD ["/bin/bash"]
# Wed, 15 Nov 2023 05:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 05:24:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:82cdc38d6d4a8f105e5928c09fada25b62831433ea5f6e4c51bda4c9ecbd9702`  
		Last Modified: Wed, 15 Nov 2023 05:29:56 GMT  
		Size: 27.6 MB (27617854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25054bfcd5aaaaab9a8b81261f4b5a2752bc79e2ef9670be2543ea4ca8151408`  
		Last Modified: Wed, 15 Nov 2023 05:29:53 GMT  
		Size: 9.7 MB (9696878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692f488bb8b766464b4e25f6f72ccf92efc432f0c10df1d1003061838b729d85`  
		Last Modified: Wed, 15 Nov 2023 05:30:09 GMT  
		Size: 45.6 MB (45572317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
