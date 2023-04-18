## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:101eaaa881d244e5b86427bd2ea3986745db049d51b2efbcbe0f1d5408efa51e
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
$ docker pull buildpack-deps@sha256:bbccbf35da61832e131a695eb66a451648c9fe24207019c396fcd9cdaf261c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81936570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2a3771bec692bafa9bf6b6d10c70540d0db0e39ed2f951458ba86af7f7e7c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:31:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:31:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43bb70e8bba148f5c5a4d50f8a5204951f795a069a2cd25b2e37ebafdd10afc7`  
		Last Modified: Tue, 18 Apr 2023 01:36:35 GMT  
		Size: 27.6 MB (27604045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673d8abcf3e237b47c181613058fc86a03ce40e22cfa4a288287dffe5ef25d3`  
		Last Modified: Tue, 18 Apr 2023 01:36:33 GMT  
		Size: 6.4 MB (6382657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc90ad50e915047a562094b5a7813b9e3f81bb7782373cfac2a9fcbf7a5574a`  
		Last Modified: Tue, 18 Apr 2023 01:36:32 GMT  
		Size: 3.7 MB (3693225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab6c6decb3beeb560234f8c7d7751604b70f7509abcff1a13111b80ae018a4`  
		Last Modified: Tue, 18 Apr 2023 01:36:50 GMT  
		Size: 44.3 MB (44256643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8a9c907da4326f88024491a3da9762d29aa85c9ae4614dc8dbd65046f9d57918
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83125345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b8ef037b71f435f2efdf17ffe0b410ad38b4e58304c29569f0b121b7228e12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:45:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:45:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc0ec898907bfe3505695fd5ae23b4cf5d6d180fdb036e767c23cc35a2abc39b`  
		Last Modified: Tue, 18 Apr 2023 01:51:15 GMT  
		Size: 25.4 MB (25437825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3711420f6b1b87fa85e1e1dde561aa26c9e0143e968d0ba9f6f98811b9e290`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 5.5 MB (5545810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741069d31363bff0e76178d15c895dcacd68407a20ce1c27f0a73ee511e61d8`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 3.8 MB (3847237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988e98a76edb96dc5fee90cb5d45db9378a4ba15f49647a098e4a4c4b888c77`  
		Last Modified: Tue, 18 Apr 2023 01:51:31 GMT  
		Size: 48.3 MB (48294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee060cbb2825a0e5c6d2c37a0f28eb460681bbc14451be3d563d3549f7365bfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80967504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2a9bce91e466eaf8d5721d6d72082a18ece9524f992f0fde72b08ce01455a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:30:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc6919ddce2a233f58cc3e7dbe578e059849f4571e49c4a84c7c981f17a89835`  
		Last Modified: Tue, 18 Apr 2023 01:36:11 GMT  
		Size: 27.0 MB (27018561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dfffa12a1f77a99f18745a89a98d7c560b403d259aaabb2ea7e8099aba267`  
		Last Modified: Tue, 18 Apr 2023 01:36:08 GMT  
		Size: 6.2 MB (6217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46934c541eaff8b64481ad9212943b45e46655b2e916d0a2a1edf56c835075`  
		Last Modified: Tue, 18 Apr 2023 01:36:09 GMT  
		Size: 3.7 MB (3653186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff58527001798506a9dc32ce859a3d047cc557aa033359f185d2451be24cf5b`  
		Last Modified: Tue, 18 Apr 2023 01:36:24 GMT  
		Size: 44.1 MB (44077916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1fd6a50b6a6df0aaae7eecf4f25a23d66698a56a420fceac58859c82334c373c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92720367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2680105e7ba022355f1f320347591ffcaa718b8d1c7fb525bcbaa2bd1de940`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:55:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11b8a0da4d0a3c624fb719be6321b9020894b77b2028fb6352c38403a1a77e6`  
		Last Modified: Tue, 18 Apr 2023 01:05:04 GMT  
		Size: 48.9 MB (48945236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:712fd37daa58220b07ef60020b33ade10599163dc40e476600099c7058b75bd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80068156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc83d080597d0511ef668ef12d04f8965d989d28c0896a33c9d5b0b3c59593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:10:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af9b4b3cd888e49ca9b73654104bd6dafd3b084b47dbe8b9aa070a6fec27c58`  
		Last Modified: Tue, 18 Apr 2023 01:15:08 GMT  
		Size: 44.1 MB (44087604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
