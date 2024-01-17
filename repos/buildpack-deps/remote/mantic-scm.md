## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:f3f2db1c56a01c25084021ae201453748b0aaf886d5e31bc9c3032d0841d21b3
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
$ docker pull buildpack-deps@sha256:99c3a2664ce84bfa30ea116c02fe29273756f572da22030b5571639edd5a7bea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83269286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a63850e7827c39043becac3e1267d9f8c55bd3a2f90355076755ccb868a1fd9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:50:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb8122a41e708f03d563c8ba7400f85d27af325fae5fbf4e00380a11f4ca1fa9`  
		Last Modified: Sat, 02 Dec 2023 02:22:28 GMT  
		Size: 28.1 MB (28070890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3950b4737b0d86b7d5a2758a2148e06120a5a73d9f1593fe22ad1a7c8e83a83`  
		Last Modified: Sat, 02 Dec 2023 04:30:04 GMT  
		Size: 9.9 MB (9907996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55d77a03c8c92313d594ba3785c087935d6e66a68604e51e8ca68fd88ee16e`  
		Last Modified: Wed, 17 Jan 2024 02:07:37 GMT  
		Size: 45.3 MB (45290400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:68057d6dd7176e621f0cae75a41735e03d0f92f6b6ef16542b077b8453c2e75d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84571261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86eb79bf5d8929617fda5afcc5c2a60cd25759a71944d703d6f2b3c44583ecaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a01529681dd04180ded851c403d6b511fd3cdbb968992acde066a32e0e7c6c8`  
		Last Modified: Sat, 02 Dec 2023 06:51:25 GMT  
		Size: 26.0 MB (26021484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae82e93d9fd7e2e58d6f4fbe50295346193ea460ba3e6b8be58dae105da215`  
		Last Modified: Sat, 02 Dec 2023 06:51:23 GMT  
		Size: 9.1 MB (9145862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7392ad5603afe7172038f23d3208c26856352898e22779a0c1f0b710d128a1`  
		Last Modified: Wed, 17 Jan 2024 02:28:06 GMT  
		Size: 49.4 MB (49403915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe1126d0b8189ca0dd26da6e64f3e02c0cf1fe3f0744777da9c4c2fd8a68aaa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82175231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0eedff44ea99734607f0977298f1f157f80dcab44aeeaca0627ea8817a55a0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:45:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1727374770547196a050f3f410bce47450929c3bd7b9e1e44530bd290614b70`  
		Last Modified: Sat, 02 Dec 2023 05:29:22 GMT  
		Size: 27.4 MB (27354913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95613e6e791d7d51806e9f81060d333d4ec85becf758d4921c664403daff14f2`  
		Last Modified: Sat, 02 Dec 2023 05:29:19 GMT  
		Size: 9.6 MB (9646950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e745cd58d981e3ca64e72f12c957b4bcf8f819a914627c6fe7dc724796d8c`  
		Last Modified: Wed, 17 Jan 2024 03:09:04 GMT  
		Size: 45.2 MB (45173368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:db1f611d93d133f71c57df195248bd230de98eddd6a8bd6d562712ba293d6119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94115890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69744f381722e251967e5aaf7c1a4ffa892f8c4ede9448e26435495bfa67bdd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6a2519a5ea0f832b2e35477f84cb47f263c19385218548bfd1ef20a7b0ef71`  
		Last Modified: Sat, 02 Dec 2023 04:51:30 GMT  
		Size: 32.3 MB (32337524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78920d0cdc2c45a2f364052f0f3ae1ca5ad03f12e0ca0ede2059df652d0396b`  
		Last Modified: Sat, 02 Dec 2023 04:51:26 GMT  
		Size: 11.6 MB (11574817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31bfd3026ccc1d71d564da8bf2c5e8e015016d2958475c67b39ec43af5ab90`  
		Last Modified: Wed, 17 Jan 2024 03:32:19 GMT  
		Size: 50.2 MB (50203549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4dcd8cbd3d41fd0f491a4c73f57668b9fa8104518c01ae5915ea8305c05f0343
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83126066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5696e6721a1c6e0d3dc74666a60e829935954ddeaacc7f54bda412c98122795c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:09:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:52:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93c83e99bb380c6b7ce7bb2c3847727b3387d6638d0e59e8c1b2eeddbd82ecac`  
		Last Modified: Sat, 02 Dec 2023 06:15:43 GMT  
		Size: 27.6 MB (27643359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3461f23023b426766431d5f005571cba59c114d2e78379817dd2d4cfbf813a`  
		Last Modified: Sat, 02 Dec 2023 06:15:40 GMT  
		Size: 9.7 MB (9697312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c8da4eeafad3966c127755e1a52d555f5d94913627b5ae46c9ef691f2ac3`  
		Last Modified: Wed, 17 Jan 2024 04:08:50 GMT  
		Size: 45.8 MB (45785395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
