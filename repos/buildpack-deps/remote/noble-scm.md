## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:f822c9792880c04fc60e2454f642f8c94f84ce7fe092e4240943978404894901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c51f14a12a16d4595e13cf4bf966e30a0ee256fbac5e7a6916e0cced9a7944e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90022765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2581458c2dd8382ec7696591d5e718acbf822c5f88016c0c712bb9be7db69b36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:59:58 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:59:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:00:00 GMT
ADD file:a0ba91d32217ea2536915535ff91264b55534a6ec7ff3d6ae86c586ba16b04e5 in / 
# Thu, 21 Dec 2023 08:00:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:53:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6e962016133a2e69bf8bb72544b211445633f148627c656908805f0ca1e2a14`  
		Last Modified: Tue, 02 Jan 2024 21:20:35 GMT  
		Size: 30.4 MB (30350118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eab6a772f8ed88e9b2ee72076bfd4fb0e94a8febad8182dcac2722aae4058e9`  
		Last Modified: Thu, 04 Jan 2024 20:38:23 GMT  
		Size: 13.7 MB (13719056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7599ddef79c8c9a66cd4f40b174c9ac5724bc3fcbaf13bdc706636285942a53`  
		Last Modified: Wed, 17 Jan 2024 02:08:29 GMT  
		Size: 46.0 MB (45953591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9a465d12b9acdc17321477af21bcace48cd3ea8685674471bd8f738bad54ef7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90482436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2b1e2046e774e9f040f38b67c6e51125880a9e3f384693fcae10ed9fc8eaa6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:17:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b1fdfccfb097e3ea8369bc634c0a794c7f5dfa00a944deeff4a97c9496acd7f`  
		Last Modified: Thu, 04 Jan 2024 20:24:32 GMT  
		Size: 25.8 MB (25769091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7239c158ae97251c79c79b045912b146acfff69748a2146ac66091ac11d3a817`  
		Last Modified: Thu, 04 Jan 2024 20:24:29 GMT  
		Size: 14.6 MB (14621580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b5a3653290438533a6e25c0661e212a2f6e7a8757b18df319541e20188a0e5`  
		Last Modified: Wed, 17 Jan 2024 02:29:11 GMT  
		Size: 50.1 MB (50091765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4c4cea528d5739d713e4b8a7d53372aa2120f4c1659c7e890b3674bc4b9094e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88930090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9545f116a0e10c0068e1de83e86750076cc0710cf1e6d7df4364d6904f461533`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:07:26 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:07:30 GMT
ADD file:747b926a2c5db1bde721d5f2e6cc257e61f094098f4ec5109ca37f7ec202e15f in / 
# Thu, 21 Dec 2023 08:07:31 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 21:02:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:48:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:894886ead4cb9562f49271af0159d0a1ca3cd047fe095546a95b2547503278bc`  
		Last Modified: Thu, 04 Jan 2024 21:08:18 GMT  
		Size: 27.4 MB (27440272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad4c764df2e8f81f9fa5b16b3c9e87d20f8f97148504bbf60a3eb3b51fc5d07`  
		Last Modified: Thu, 04 Jan 2024 21:08:16 GMT  
		Size: 15.5 MB (15513863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae3ebef7d3c1616351532aa160c17b0911557b386f40db28b80fa777f1e64d7`  
		Last Modified: Wed, 17 Jan 2024 03:10:22 GMT  
		Size: 46.0 MB (45975955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4dc0d23af7170e6cc5d5796ab42204acd3d1b2fcd636d8c0f192593c9f5381a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101460725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a3258e9ec283ace102ecb08f077f530f015e2cd2a55a058575cb7ec8492d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:46:19 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:46:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:46:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:46:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 07:46:22 GMT
ADD file:83a18fa01ec4574671ff01727c2059a3f114915594312ad939999fb6266c8b85 in / 
# Thu, 21 Dec 2023 07:46:23 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:30:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 20:31:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f7ae3c70a47814103cc56d7659dc773a9caf5ce8df4d8324b88d9b5043e063d4`  
		Last Modified: Thu, 04 Jan 2024 20:38:35 GMT  
		Size: 32.4 MB (32405112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a6c7c9e8ceb49b67e3dbdacee3d70552db6ae83ceaea6d637dab7c45794b13`  
		Last Modified: Thu, 04 Jan 2024 20:38:28 GMT  
		Size: 18.5 MB (18547889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac382586005ae922fe6b9228080ee73150c2591819f6db9347fc6a9316dd0b86`  
		Last Modified: Thu, 04 Jan 2024 20:38:54 GMT  
		Size: 50.5 MB (50507724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:167f8d3384613fce84df28ed853cf2f17b96b109b341e9be8881b7f69253d77d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91644083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226ec3c7773350f8e9196d9c51a13d17be2fb1f1795c312912446e4946023f9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 20:46:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0eb0ee1ee32a505c711b23ae33e7ecc888899622d95c7e982ef82dbb529c5d8`  
		Last Modified: Thu, 04 Jan 2024 20:50:14 GMT  
		Size: 28.2 MB (28174524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02199b1c3761965bf141c9010678515a9c50e39cc89d2a830d1dd5d17aa25bc2`  
		Last Modified: Thu, 04 Jan 2024 20:50:13 GMT  
		Size: 16.6 MB (16609480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35074eaa320e26e298de6603d259e32c732e9b59403ef9ded95fc308e880cdb`  
		Last Modified: Thu, 04 Jan 2024 20:50:27 GMT  
		Size: 46.9 MB (46860079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
