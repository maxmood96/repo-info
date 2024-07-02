## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:19bc4f95f87bb2f0975c5f1090b6a565022a1f890e19af055e3e4f0d701af074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5d9cb6dcd1cd3180bf36be7ce1fd0201ff08d3a2e81d30ffe7315220545f6d70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76986152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4a1ee970e379a731f912d64cc05bb22e84dae7cf91b51acc2d8790d824a2a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:55:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966d1a9d7dc827a9dda799795c07c44b594a52122c0b1c90242bab120d580c8`  
		Last Modified: Tue, 02 Jul 2024 02:04:36 GMT  
		Size: 39.5 MB (39454836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f82d4287805b367c95ad99bf810f131a7294023636c1db0f7f7e254a1db9fcba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76769191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132a36536fec47518fa8472beebbe070410f5a78ffbf2eac862b0670f3567f9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2f711ae14b51dbbfedf8af05176ef3a326ae9cd221d1a2981579493b38fed`  
		Last Modified: Tue, 02 Jul 2024 01:43:31 GMT  
		Size: 7.0 MB (6992114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19939d362c9742ec7a32f61568520eb8438dc48cbc1335ffd7fa62bf170ceb4`  
		Last Modified: Tue, 02 Jul 2024 01:43:51 GMT  
		Size: 42.2 MB (42243066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:55fb4b90a5186d3029858ed5fb1e52fe778753ff241fc82ae91e64d794a2652c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74812514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628d80babb0f665e8b36e0039db96d6c42479562b28379fa8b430ab025a687c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:57:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aac2765dc6695d0f69e7852783ff14ecb83d04db68edc06347651928706052`  
		Last Modified: Tue, 02 Jul 2024 04:05:26 GMT  
		Size: 39.4 MB (39378111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8161f7c68935700123953ccf08bcec8ca4cddc7e431090a883b879c44eda157d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87544616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fbdf7b7eb43e810daf796858cfbdbb7267bbb2d358c2ea24f9556a300c3c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 01:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:58:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49bd859389beb8b466c6fe9ed50ae354c6b62b4ce551e29b2d4d77740b6bb04`  
		Last Modified: Tue, 02 Jul 2024 02:09:08 GMT  
		Size: 8.2 MB (8190455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82dc8e44a33d0f6fbe0c131eeb8268e1997857f2a63a77b883c6c1e387f308f`  
		Last Modified: Tue, 02 Jul 2024 02:09:30 GMT  
		Size: 43.8 MB (43765840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4a9437676ab21da7b3ad03457706ea309e2494fe018e775af025e81eb288d464
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75061033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473e03988f89693816397ff7caa90aa86fe7f6fb6879e6e98362da2abe59e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 03:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:40:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ff6b47b92963b3c5a902678f8100c7d76dbd36317ab5e839cb79cebd7a415`  
		Last Modified: Tue, 02 Jul 2024 03:47:51 GMT  
		Size: 7.0 MB (7003262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693aac14b0c492b501054836b25b7b1ce8545575960bb0ddd3c31b6bab5bf990`  
		Last Modified: Tue, 02 Jul 2024 03:48:05 GMT  
		Size: 39.4 MB (39420301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
