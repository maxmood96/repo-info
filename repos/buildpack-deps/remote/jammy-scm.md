## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:3347f2dfd51fd5a989d0efef1e408248aeb86cbe84193727b2b3d785b0486c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3bb7d3ba4a80fd483a455822fce478f604dd7827f989977aa93e7766673c3813
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77000994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd888b4f921a3f2e51866a336cc5ed86111ec15ec8549bf15961b9518fd27f86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321cd5ae2a05dc61774ea917ff22fb166f1b67cd06921fed6f4270e0caf4c28`  
		Last Modified: Tue, 17 Sep 2024 00:51:03 GMT  
		Size: 7.1 MB (7091507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0473099c79c1b90b89fe006a5bd9596b9ece18ac24a399144f285ccf6c7d77`  
		Last Modified: Tue, 17 Sep 2024 00:51:19 GMT  
		Size: 39.5 MB (39469554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ca89d3c84aac26f46e6bb0cdeaab9f13a9e6ef1232c9f88d738920468cee04c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3865fc6395b60b13dcf7604154e8af62468ec80630d7e29c3d8fa721f79324`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd0a1cae54a28ec0e599785afc38d05160d3f8686cf6937d69452f78d94839`  
		Last Modified: Tue, 17 Sep 2024 01:41:53 GMT  
		Size: 7.0 MB (6992206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f084e39677777a3c9198d380890db30c595eeb224db5b12fee6f43e975e333e5`  
		Last Modified: Tue, 17 Sep 2024 01:42:07 GMT  
		Size: 42.2 MB (42247087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:34b279fc4700c4c672e2f22e3280bae0cb0c280f525b541c37ca65d60825ee44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74813547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704307d21ad72ec302a4cc79016a0bf4a76c059c059bed698eb499cb6235066`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd83996b821ee5c0621feda52f2e1c48acc45c95fdbed9c47ac71c763ee53ab`  
		Last Modified: Tue, 17 Sep 2024 01:29:00 GMT  
		Size: 39.4 MB (39382970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1b8326726907980331fce56e29898f8fa15de30f322f5a2acd9f53783f8a9988
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87539742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee69e7ca45d862356910e271c2350fdd3b4e2c808aa97078e0189a2c53a3fed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8d72dbcfacd5ab6c85442e53b4d619dbd9d2a9f763870e1b9832f9d586aae`  
		Last Modified: Tue, 17 Sep 2024 00:52:00 GMT  
		Size: 8.2 MB (8190210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3363e80d9b6d155f0ae139ce77aa32fd94df6eb46f50a3bec738d1033d8f32`  
		Last Modified: Tue, 17 Sep 2024 00:52:23 GMT  
		Size: 43.8 MB (43764044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:543266395b2597cfe93dfa4c7296684c535b15b50cb1ac4571918f69ee613316
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77120987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2661a6202957a6278bc4f96ae15f34541d0e2a163f56b6d81d87b8831f4f07b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 02:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48358b2555c9c945ff48896d23870bf2a38655f2cab34ae238a1816fb94aba25`  
		Last Modified: Tue, 17 Sep 2024 02:31:37 GMT  
		Size: 27.7 MB (27709783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a86100759b4ac9be7dfc46e76bcd08d87c85fcae4c74ca2e30103bf5139f1d`  
		Last Modified: Tue, 17 Sep 2024 02:31:22 GMT  
		Size: 7.1 MB (7100493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8da1cbeb5ba78f9eb56920d49a58264a0e7f14bbbb546d6b818c307ca003982`  
		Last Modified: Tue, 17 Sep 2024 02:32:23 GMT  
		Size: 42.3 MB (42310711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ee2acc822f0c058c87d4ef405f40716f7a0c2f268e4f43d66b4f709e2358f9ae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75045319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c98d55db1472725ecfd27f682daeb79ae243193ac474e45aa974d502e56786`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Sep 2024 01:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d70a720dea339721e95dc7bc3a2036d1a65f69be3cd6c8481635437b7a7155`  
		Last Modified: Tue, 17 Sep 2024 01:28:17 GMT  
		Size: 7.0 MB (7003532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200351c809009210c9ff3d95069658520c0808d693cf45463f14174972dffc8`  
		Last Modified: Tue, 17 Sep 2024 01:28:32 GMT  
		Size: 39.4 MB (39402519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
