## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:bdbbfbd7bd9aeb32678f8a9f6d423e0d5709af02e0e4a33e70e99b2a86658aad
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
$ docker pull buildpack-deps@sha256:41592dd1e67dbffba26634f00619f5da6af28bfaefed9cf9475afdaa03acbf6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85728568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fba109e84f956fa8db5ad6c4f1d621aa0184f493c6f92c176ecf3b10843533`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:48:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ccc37bca66e7c29e0d65a4279511fe9a93932a4bb80e79e95144f3812632b61a`  
		Last Modified: Fri, 16 Jun 2023 01:56:54 GMT  
		Size: 27.6 MB (27612943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7beeb5a79f9bd13c90ee4c9f68636fc642df773adb1bd04e27e2115f6c12a6d`  
		Last Modified: Fri, 16 Jun 2023 01:56:52 GMT  
		Size: 13.7 MB (13744092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a98e278987c0da01adb1f6145dec78bd526ecc11c227e2e74c48de9cd72c40`  
		Last Modified: Fri, 16 Jun 2023 01:57:09 GMT  
		Size: 44.4 MB (44371533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5a6012c64abe5a1e4977712e462e6802d4c5e7a02f2030a15e71b72ff3dfe57a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86748441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23973e09ff69a4949c38d23ac559b76967b561c2e71a9c4d1998f800fc603a88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:49:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:50:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca5128fe76949cc104af7f40ce0f7213fe093079077d47dd525fa0189090c57e`  
		Last Modified: Fri, 16 Jun 2023 00:59:51 GMT  
		Size: 25.4 MB (25432780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8ca764d56bdf14c46fabd5c4e2e988ce166d01c8c0631d7c345802ace7bf1`  
		Last Modified: Fri, 16 Jun 2023 00:59:50 GMT  
		Size: 12.7 MB (12662932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b3e8b607724476a55e2e23faa2859f1e37c17323d12df2f9b87de3745b98e3`  
		Last Modified: Fri, 16 Jun 2023 01:00:07 GMT  
		Size: 48.7 MB (48652729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5da19ddb7546538c21ea08a02600a19310d9b4e70bceb38b8d28b5ab6e5dc414
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84600697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6d65056494c7aefc18c52c927cc20d4bae8d5849b343a2b3d8b5258fd8c6d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:24:02 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:24:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:24:11 GMT
ADD file:8af4f6767fc5b6665bedd4600c0601ee7d7f803de51e979a40bd3d6ebcd25f95 in / 
# Mon, 31 Jul 2023 17:24:12 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:39:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc3ebe95800c7b88cce17a04cb6a4e51211ef73656bd15c0885a6f96b173aeef`  
		Last Modified: Thu, 03 Aug 2023 00:50:53 GMT  
		Size: 27.0 MB (27031709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c53b82c57224a6aeb0716a4227436ebcf006fbd33ca9346c8875243d0ba942`  
		Last Modified: Thu, 03 Aug 2023 00:50:50 GMT  
		Size: 13.3 MB (13333570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf1c6caaac9b5afe5c21f87c81ea52cb2f170dc8014fc97564f9337986ac802`  
		Last Modified: Thu, 03 Aug 2023 00:51:07 GMT  
		Size: 44.2 MB (44235418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c5a83ab3770b99e11c2b4445afb7ee1d926562a534194746e3288c6e0f2fc9b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96926153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c299a6b52971b8d036a8ccadd60c639e7831b2c4f677f2882df75e523a441b7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:11:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a58a0b662b0d4d5e271c7c17f35795b5782a33c69a079e473f7c2303bee50024`  
		Last Modified: Fri, 16 Jun 2023 01:28:52 GMT  
		Size: 32.0 MB (32010412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6f165de89ef5a3a93777200dd180f02a8fc30051f7eb6267300a3e6f27ae1e`  
		Last Modified: Fri, 16 Jun 2023 01:28:48 GMT  
		Size: 15.8 MB (15841962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06312954ebad2b0995222a924fae1923e9b3c87aa73ff14beea981d9235b706d`  
		Last Modified: Fri, 16 Jun 2023 01:29:15 GMT  
		Size: 49.1 MB (49073779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bd38c179a2089a2fd31e1411fb8039d0fde3144a93ba16a28ed3fbb8a64e1b36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84525179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f1cdc23fc8fc1b831ac6c632f34b97cab184a6272ff438b716ebe8e1e0e1f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:25:09 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:25:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:25:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:25:10 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:25:11 GMT
ADD file:02e6a6123ef99d36f86e3e53231b3ba93c90b4ac9fc0bdebe8f01f2a6c2efb4e in / 
# Mon, 31 Jul 2023 17:25:11 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:12:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:13:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec64faa69090fa13dbf3419726044381d0c7137866daa46daa6a85f785a5389a`  
		Last Modified: Thu, 03 Aug 2023 00:21:59 GMT  
		Size: 26.2 MB (26244138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6910656a90f2717882b9ec910b9f54fd6d237915853a5ffd4b160913158408a2`  
		Last Modified: Thu, 03 Aug 2023 00:21:57 GMT  
		Size: 14.0 MB (14005556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c57b46166fdc730877dcee11a4a6741fc625ecc917bc6560eedc5c318870915`  
		Last Modified: Thu, 03 Aug 2023 00:22:11 GMT  
		Size: 44.3 MB (44275485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
