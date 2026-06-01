<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260531.0.538839`](#archlinuxbase-202605310538839)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260531.0.538839`](#archlinuxbase-devel-202605310538839)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260531.0.538839`](#archlinuxmultilib-devel-202605310538839)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:40ec92af4b7de7127251038f2e1af7978c1dbc1625e4c7d23b7a89eee05e5a58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:ca64cafd0d2e1fd5744d0f607f11a0b33be173790665c9e2931f756ffbb0a37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131712404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd549cf9ec5dc1c2a348412027a9b3bde3d5ed00698c23c7e24b0f9f16eefef`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.version=20260524.0.535079
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.created=2026-05-24T00:12:57+00:00
# Tue, 26 May 2026 18:59:31 GMT
COPY /rootfs/ / # buildkit
# Tue, 26 May 2026 18:59:33 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260524.0.535079' /etc/os-release # buildkit
# Tue, 26 May 2026 18:59:33 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 18:59:33 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7e3ad9f3b68bf3c61b23f847702a58c98f1475ba219c285f7bf497551fb36f9`  
		Last Modified: Tue, 26 May 2026 18:59:59 GMT  
		Size: 131.7 MB (131703722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d633867c6969f24ab449103f26513eb33bc780f1566a72329f116d418cc54bc1`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 8.7 KB (8682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:880c90ec7e95b7cc9fc6ab5292ec96200fe58b7c6a8a2f803d0c8ef7b6a38238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fff2f70ac70fb49234ecc8f90ad340573e13c497911207a21643c14ffdad6e`

```dockerfile
```

-	Layers:
	-	`sha256:c9e51910311b5b0a345291c8a183f27420ebe6410fcc6e29b87f18ac614c32e2`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 8.2 MB (8181157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6ead6609704b294727cc86e83a37930b390b63cb33b0a48dabffc75fc251c8`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260531.0.538839`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:25074821d28e54a0bbbd87a88d392f1489be9bd815ee5c60744be6e57fd500d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6d08b7067286234b755a28340b6bd89f3a2289233dbca3c361464f27ecae8f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303791039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580435224cc79643afa10d15c96e18bcd2e5b2f6bed0f6d9ca0cec3088c0561b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.version=20260524.0.535079
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.created=2026-05-24T00:12:57+00:00
# Tue, 26 May 2026 18:59:47 GMT
COPY /rootfs/ / # buildkit
# Tue, 26 May 2026 18:59:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260524.0.535079' /etc/os-release # buildkit
# Tue, 26 May 2026 18:59:54 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 18:59:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0918ff50f07eb1e93987401d7008971f93c893f4a592c183723f4618bcdb15cf`  
		Last Modified: Tue, 26 May 2026 19:00:51 GMT  
		Size: 303.8 MB (303779612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becec186e69bb6eaf326716f41694848554950a23f6583c61fcf4d37f35558d8`  
		Last Modified: Tue, 26 May 2026 19:00:43 GMT  
		Size: 11.4 KB (11427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2114986abe1f78c7f73934aa10e4bcfdaf7abda58883c9cd9f8cbbf8b0aa38bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14396300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67dd7c236d3cc3a189f9b37e032ccd58fc18b49153d53bfed8b20e21436b1dcb`

```dockerfile
```

-	Layers:
	-	`sha256:4b5809322b6a47d72ba0c1c44175d0462f0a744516e79c2a700033e39e941958`  
		Last Modified: Tue, 26 May 2026 19:00:46 GMT  
		Size: 14.4 MB (14384588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670480bc2b7f09b900dadacf69e0d3601e43f9088510995516a0f58d4023721c`  
		Last Modified: Tue, 26 May 2026 19:00:43 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260531.0.538839`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:40ec92af4b7de7127251038f2e1af7978c1dbc1625e4c7d23b7a89eee05e5a58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:ca64cafd0d2e1fd5744d0f607f11a0b33be173790665c9e2931f756ffbb0a37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131712404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd549cf9ec5dc1c2a348412027a9b3bde3d5ed00698c23c7e24b0f9f16eefef`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.version=20260524.0.535079
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.created=2026-05-24T00:12:57+00:00
# Tue, 26 May 2026 18:59:31 GMT
COPY /rootfs/ / # buildkit
# Tue, 26 May 2026 18:59:33 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260524.0.535079' /etc/os-release # buildkit
# Tue, 26 May 2026 18:59:33 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 18:59:33 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7e3ad9f3b68bf3c61b23f847702a58c98f1475ba219c285f7bf497551fb36f9`  
		Last Modified: Tue, 26 May 2026 18:59:59 GMT  
		Size: 131.7 MB (131703722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d633867c6969f24ab449103f26513eb33bc780f1566a72329f116d418cc54bc1`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 8.7 KB (8682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:880c90ec7e95b7cc9fc6ab5292ec96200fe58b7c6a8a2f803d0c8ef7b6a38238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fff2f70ac70fb49234ecc8f90ad340573e13c497911207a21643c14ffdad6e`

```dockerfile
```

-	Layers:
	-	`sha256:c9e51910311b5b0a345291c8a183f27420ebe6410fcc6e29b87f18ac614c32e2`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 8.2 MB (8181157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6ead6609704b294727cc86e83a37930b390b63cb33b0a48dabffc75fc251c8`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:55a7352e9b556656a0eed60bb72f4a546b5d06aec060fb295d7e98dc02c98feb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0f699314eda17eb77f2026c693c35fcba214b984ce0564fe4e9440d86d8d7f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.2 MB (326164515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce52ca4c5ef44376d55a03d96a991b4d9b3a0d2be2d8a6d78806620b43a1d48`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.version=20260524.0.535079
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.created=2026-05-24T00:12:57+00:00
# Tue, 26 May 2026 19:00:10 GMT
COPY /rootfs/ / # buildkit
# Tue, 26 May 2026 19:00:18 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260524.0.535079' /etc/os-release # buildkit
# Tue, 26 May 2026 19:00:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:00:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3f752e590d610a34618f941771d6c6bcb73c7309514378d23abd9e46b4d49764`  
		Last Modified: Tue, 26 May 2026 19:01:14 GMT  
		Size: 326.2 MB (326151948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac52b4c2ab0b6fc7dae672d718111b3a451ac4c49dbf674d9df2c9f0ef962fe`  
		Last Modified: Tue, 26 May 2026 19:01:07 GMT  
		Size: 12.6 KB (12567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:cd2cb65e3ac46f802b0feb77b7a0361074878ffa6cfa113d241a8753d23eaac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14667097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa6525b6a729e8ee43315ee7515522b0e83b2c3305c08022f602e7e311ce799`

```dockerfile
```

-	Layers:
	-	`sha256:cf7c77ac1888f825e7cbfba64f28b61719fb1548c5857f8970d2663dab501035`  
		Last Modified: Tue, 26 May 2026 19:01:08 GMT  
		Size: 14.7 MB (14655329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31c79f7d6fa78665fce270ef22f1a6008035eaaa6479d22b6def9cf1b05b72`  
		Last Modified: Tue, 26 May 2026 19:01:07 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260531.0.538839`

**does not exist** (yet?)
