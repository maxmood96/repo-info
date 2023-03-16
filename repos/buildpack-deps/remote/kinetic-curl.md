## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:93c7e62affa73f33a0a50e0044ea64a76772664bb874b863705c70536e6d651c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c1bef77a747c1b0d0e2e1943063d242d97b14090c6fa5a4396872c2e5e86cd7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37884733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f070e17b881f324f200c61c5d2fbd431ae10cc95570becf16c69abab64af58b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:43:07 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:43:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:43:09 GMT
ADD file:18f562911635a03a9bf9e5fc22863fc2a78a64f7d35c7daa59f2d609b7ca055a in / 
# Mon, 20 Feb 2023 11:43:10 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:34:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a10df61efde6b7f0cf3fbf848a5bed1c943a54e13566f30ef6a0cc6f259a2f33`  
		Last Modified: Thu, 02 Mar 2023 03:44:58 GMT  
		Size: 27.5 MB (27479398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a9f9f71b0155b4b832dcb9bfbf542389507996cd93239b78300535c9421961`  
		Last Modified: Thu, 02 Mar 2023 03:44:55 GMT  
		Size: 6.8 MB (6770219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710e0dcd6284a414a9f90e76d5555002980ba77c51b01d6a812e56d2c2d94d2e`  
		Last Modified: Thu, 02 Mar 2023 03:44:55 GMT  
		Size: 3.6 MB (3635116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4af883c5eab3c2380a46236ca3ca95f3048243965b2e897814c48e8260dfa2c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35633477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094d55cec9f8dc3d95b8ee21b11560284d162a4571f93b0b44109e9fe8e3d0cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:55:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:55:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:55:49 GMT
ADD file:827330b6c59e67c5d2edd3ceb3492b97865b15f9246f14710f478d12e94d2048 in / 
# Wed, 08 Mar 2023 05:55:49 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:56:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:56:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6408fcff70bde57e1c23e7502a9476939cc569e2eff3e9e9adca350cb5b4dac1`  
		Last Modified: Thu, 16 Mar 2023 04:10:41 GMT  
		Size: 25.9 MB (25890803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467248c617f5da80617561605e184647a03bc6ee0731094ea5fa1a10a9d97d12`  
		Last Modified: Thu, 16 Mar 2023 04:10:38 GMT  
		Size: 5.9 MB (5941308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed064758ff6efc72c5bfa16404dd5e5a7196c6704c9bfce54fffbe511f026`  
		Last Modified: Thu, 16 Mar 2023 04:10:37 GMT  
		Size: 3.8 MB (3801366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f7410e86839d94189da0421368263daad23e4532602532ebebb243959a6589bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36907970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11201af935ca582771cd9c1d5a25562f6956d2d83b5561f776ff20235996f3a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:57:57 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:57:58 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:57:59 GMT
ADD file:884e00dc91bf6d392fa3d117913cc2534177128322d89137bfb8b2734bc38579 in / 
# Wed, 08 Mar 2023 05:58:00 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:12:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:12:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:254a784e837e29e485a63351d1a7aba22a34cad2c55e16264bd25ec0add89463`  
		Last Modified: Thu, 16 Mar 2023 04:24:12 GMT  
		Size: 26.7 MB (26703428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c5262eba6308f5bd6759d8fe45a1d30f1c39e36af3ffc10b11c84e335e3cf5`  
		Last Modified: Thu, 16 Mar 2023 04:24:10 GMT  
		Size: 6.6 MB (6600337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d93a07df4f2da69d3c85f944e8fa42f4e401cfb09edbff605d5863469a8c37`  
		Last Modified: Thu, 16 Mar 2023 04:24:09 GMT  
		Size: 3.6 MB (3604205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6760f29c9bdcdc308fcf3afb3ca98c719d1c0c3e8c5a5bea33cc33c3db2550d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44209744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14fbb219e4d625d407f193f60f7c075595d470a92f731343a064f26b3a6c72a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:58:03 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:58:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:58:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:58:03 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:58:06 GMT
ADD file:583061e8201c03de4747860e734200b6c35b449443a1382ad8e8efc6f7e9ea13 in / 
# Wed, 08 Mar 2023 05:58:06 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:30:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6ec1f8fff860753bb5de879722c39643b2fecee25466efe51120479c4cd7647f`  
		Last Modified: Thu, 16 Mar 2023 03:52:17 GMT  
		Size: 32.1 MB (32098861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00fc14ce944c08bb40e1940367da097dd6113e4621903eedbeb83cf9caea6cc`  
		Last Modified: Thu, 16 Mar 2023 03:52:08 GMT  
		Size: 7.7 MB (7748081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75e7525a0f6794b3368a8aecf0b1c8c88ab38a7de79a51f2cc03b69581df2f`  
		Last Modified: Thu, 16 Mar 2023 03:52:07 GMT  
		Size: 4.4 MB (4362802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d2366f9c8542e47115c50c026f6cf9ccda7aaf6b859307b5ca9f1f1c0cf8a50b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36116478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee7ee58323c7f6349967f769687f47de069565561ee8264351d32a8d0ecd22e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 06:11:04 GMT
ARG RELEASE
# Wed, 08 Mar 2023 06:11:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 06:11:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 06:11:04 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 06:11:06 GMT
ADD file:974d67ca1d5bcaacbc707820609d36af0d7ed3ff7179a702a4aa56dcc43f79f3 in / 
# Wed, 08 Mar 2023 06:11:06 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3e94c7036e7dc9a2d6666b2f4fc00019c0540bd3edd16e54289a9d6b7134b349`  
		Last Modified: Thu, 16 Mar 2023 02:03:35 GMT  
		Size: 26.0 MB (26029370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc60d216fdfa5dd36e7941c80e0ea9d1b8c692a8c067ad512585b6ae40bd6e99`  
		Last Modified: Thu, 16 Mar 2023 02:03:32 GMT  
		Size: 6.5 MB (6461878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c257c035538e42c9fb24b73041a70d92b99378d720c80bc418d8ed7900e2d15c`  
		Last Modified: Thu, 16 Mar 2023 02:03:32 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
