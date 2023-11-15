## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:fdd84b5fb072cd9015e72499e405b6c2ee6071d354e22f49309744b75abe40a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:921a763a77cd772742a6ae544a5bd71b4411f92a999be5d1d7fed1684ddac2e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37974507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287d7639ff0677fdfe2b1eadc6efdd695a529748505a9cbdc44b29355b92125b`
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

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2913f2f84d97ff1be7ca139b43ce4e8d05cfaf7ed3248b39aa9e6a70b154ea91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35163344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cd33ac4877ec60e73bfb24bb572ad8088801b2acdcc70314770203d15b6c91`
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

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d649d5fa7ae482f135330be776368c49ff5d30b7336734c39ad94af9a6064874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36985512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ce70cb7143b41128b73de1bc7c1520314ceae722ab6e435381a4fd31188a78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:03:02 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:03:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:03:10 GMT
ADD file:9e750ebbbf7e47a121d153e6699006776ea61b04b6c8e31556600483a020f617 in / 
# Wed, 11 Oct 2023 18:03:10 GMT
CMD ["/bin/bash"]
# Wed, 15 Nov 2023 06:17:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b743c812db4b2a4cb933b4107dd5408c786d034c3bcff4d162d02e20587dce07`  
		Last Modified: Fri, 13 Oct 2023 06:40:38 GMT  
		Size: 27.3 MB (27340045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e717ff89b8bce5f5201b6827c6ed6615c39f2b52f5b0e8ca3d659d049b51e6`  
		Last Modified: Wed, 15 Nov 2023 06:23:55 GMT  
		Size: 9.6 MB (9645467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bcab01774044541e169e955e9d52762f736b27fb6c76d029381b6162dedbfee9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43904748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbce8aeac751517d845efadce6fb839eff255b2c00e279e01eeb686343d3d0d8`
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

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e3fb9abd82bd63f435954245545251574327c9881255d2db0ca53940bda40d64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37314732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64946e8ba5952759944b3513696715ee3fc336e4cb5f02dced4113a84b7fb861`
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
