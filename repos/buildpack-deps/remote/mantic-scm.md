## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:16b936981452b9f44a0a58d93eed6d0a35006f36e6fe677bd073e94751c9b314
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
$ docker pull buildpack-deps@sha256:7ac32abbc5bd894e66ca36355e4212564fcd2887d97a91990b4ca4f7310cffe8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82727335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfb289c2b2e169763b6524ce729573508c902bb6de42094621683a77c16840`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:48 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:48 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:50 GMT
ADD file:432d92758637d8e71c4a18c3b453d3c8130fd1fa31fd3cb9e60ecd32cdd17e07 in / 
# Thu, 30 May 2024 04:40:50 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47248bd506cc99fc9466a84ebef243c953353062848a716b6d0a2446b49cbb81`  
		Last Modified: Fri, 31 May 2024 21:47:48 GMT  
		Size: 28.0 MB (28037220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b6e38ccc7cf178ab294b2855e3e53111f52e99dbfea0c356d475ee927c25e`  
		Last Modified: Wed, 05 Jun 2024 04:48:59 GMT  
		Size: 9.9 MB (9911776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea509a29544edd67ece4c5006665316329880fdef08c2b42d62e31799e97bd9d`  
		Last Modified: Wed, 05 Jun 2024 04:49:16 GMT  
		Size: 44.8 MB (44778339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dffdddc92193eb796ffb33065b30796f20d7c1df54f8671fca0fbbe6df617272
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83783027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec225f12da4434d781ad9b074870e390b9605010ac72f3262a67900eaf8b87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a04cad1e2168093eb69d36324c57c8d5a592597dc124473e47a7734b4ac780d`  
		Last Modified: Wed, 05 Jun 2024 03:53:36 GMT  
		Size: 25.7 MB (25688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be993b7551c91005764db4f62ec9285d2322d78dbed6f84b24965e75ba4bb29d`  
		Last Modified: Wed, 05 Jun 2024 03:53:33 GMT  
		Size: 9.2 MB (9152175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76642a0d8c917f8b4762138fba3c9de67689f5a5e5de9b64d3f6f72b20f70709`  
		Last Modified: Wed, 05 Jun 2024 03:53:52 GMT  
		Size: 48.9 MB (48942204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:825dfb37fcb76a6ccf6308a4dd9750b16454cef52968f7d78a658e6a864e02ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81793702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb2aa33211a1c117b30f56ba7edbdee935c9c5afed0dcdad799e3f0d6764541`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:50 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:53 GMT
ADD file:f520e3c120f5d02fd61bf37254a519532f628d0cb237f46acf51ac08b1c2a180 in / 
# Thu, 30 May 2024 04:35:53 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:21:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60297f27bf43ca95ebbf1c02c2a26d7a22de85fdd6374f3bb09dee47d06b9cdd`  
		Last Modified: Mon, 03 Jun 2024 20:07:10 GMT  
		Size: 27.4 MB (27380847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de948efc2730b49bebe3add459cfc2fd3681636c1bcc8739d8fe218de52f6ca9`  
		Last Modified: Wed, 05 Jun 2024 04:35:41 GMT  
		Size: 9.7 MB (9665606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a7640621fe982a10d3dda8496aea07502c6024b26780042604c39f807ebd4`  
		Last Modified: Wed, 05 Jun 2024 04:35:56 GMT  
		Size: 44.7 MB (44747249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2d41584f5bfc5f74f4c9ee4219d2aade02e1784f0d21489120454fa0324cc094
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93554523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5df9795dcc60d79106b41a88b1d51bc5d039e9e8d9c75343bb8e632b4d8813`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db7b14ff19434de4b9e4762b8b845a87a0d56130bdee33d4a49f233abb62c9b`  
		Last Modified: Wed, 05 Jun 2024 03:49:19 GMT  
		Size: 32.4 MB (32350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e104d2d8f80f552c85787a29c9846d9ccc245d14399c5c14a1b07feae431275`  
		Last Modified: Wed, 05 Jun 2024 03:49:14 GMT  
		Size: 11.6 MB (11585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb7ced059bf2a43a1fe9d833ce19fe75a8eaf293da574dd45c14836e77cdf4`  
		Last Modified: Wed, 05 Jun 2024 03:49:35 GMT  
		Size: 49.6 MB (49618077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:81f715a4d61d44a0bf4f15848f950e8b70995191779291a6e65abe51232a7597
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83698162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370f2491b2f8c94c9a815eee1e1e01960197280f0ccae7e259ca143c5dd045ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eee394775ffd8c11d94a145d72ab3ed77cb072ed5a12669c7ac4615a277e23a9`  
		Last Modified: Wed, 05 Jun 2024 03:36:21 GMT  
		Size: 27.9 MB (27891404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74c9a6e2d4a8987c978732b98b406a9f7977e0c8dc80bd843a38a97029cea`  
		Last Modified: Wed, 05 Jun 2024 03:36:18 GMT  
		Size: 9.8 MB (9759019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8180965f353999389ac9a5a3880e73af3fe29a168b55d1e7cf69c49184ef1d`  
		Last Modified: Wed, 05 Jun 2024 03:36:33 GMT  
		Size: 46.0 MB (46047739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
