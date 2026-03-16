<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260315.0.500537`](#archlinuxbase-202603150500537)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260315.0.500537`](#archlinuxbase-devel-202603150500537)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260315.0.500537`](#archlinuxmultilib-devel-202603150500537)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:70aace0bf67d14280ca54bc2c7ee15c5fff62684131b34ab38f99f730b643733
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:8c825387fab3f1f20502e4480e3c81c2455615e5fab7fc53a7d693f528cc443f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128325692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05596ed38debe7bb76b70bd7cac20812683948c81fa54aca06e4b1cac83496dc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:42:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:42:17 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:42:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:42:17 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2317a1c19ffbba80187e7b5124537a6007649864a07d2f77a5346055a49966bc`  
		Last Modified: Mon, 16 Mar 2026 16:42:43 GMT  
		Size: 128.3 MB (128317108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f579859357ed6e23f35449a1e7e0afd4140ac522c79637d1cb140414dc8717`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 8.6 KB (8584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d7846d82033aee8945041d7aa0e81884777878a29b9cc15ef063a8f8bd07ae49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8116305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef45d46f67f423d881d1b2096dc15fdd3f84d2ca7702eb1ffc14b4a5567cd49`

```dockerfile
```

-	Layers:
	-	`sha256:10e9b9e7d67c83c472d1bcb62f1b95c124fec9ac5684f7da313c5c3b92835b44`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 8.1 MB (8104376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283dcc06773771146ab6cc8885a308844c6b6559a343c09c15a00e45e5860eb4`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260315.0.500537`

```console
$ docker pull archlinux@sha256:70aace0bf67d14280ca54bc2c7ee15c5fff62684131b34ab38f99f730b643733
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260315.0.500537` - linux; amd64

```console
$ docker pull archlinux@sha256:8c825387fab3f1f20502e4480e3c81c2455615e5fab7fc53a7d693f528cc443f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128325692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05596ed38debe7bb76b70bd7cac20812683948c81fa54aca06e4b1cac83496dc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:42:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:42:17 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:42:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:42:17 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2317a1c19ffbba80187e7b5124537a6007649864a07d2f77a5346055a49966bc`  
		Last Modified: Mon, 16 Mar 2026 16:42:43 GMT  
		Size: 128.3 MB (128317108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f579859357ed6e23f35449a1e7e0afd4140ac522c79637d1cb140414dc8717`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 8.6 KB (8584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260315.0.500537` - unknown; unknown

```console
$ docker pull archlinux@sha256:d7846d82033aee8945041d7aa0e81884777878a29b9cc15ef063a8f8bd07ae49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8116305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef45d46f67f423d881d1b2096dc15fdd3f84d2ca7702eb1ffc14b4a5567cd49`

```dockerfile
```

-	Layers:
	-	`sha256:10e9b9e7d67c83c472d1bcb62f1b95c124fec9ac5684f7da313c5c3b92835b44`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 8.1 MB (8104376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283dcc06773771146ab6cc8885a308844c6b6559a343c09c15a00e45e5860eb4`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:87c122fd99e648dc1a12536d181d40bd7a27ad3201c4bcfa55ccf219b42f4806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:45fe50716152d2b7b43c3a781a2e4c428fd3005baa44b0c4caa59a5fa5dc050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245961571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f26d654f62f77eb5ff99540cddcfdaeeaa8fac2bfc0b97f2fad93e148a2475`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:43:29 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:43:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:43:35 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:43:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3485bafd682693abf8d3d75ec09212f3e00add355d8f933af56e0604c74bf8b7`  
		Last Modified: Mon, 16 Mar 2026 16:44:16 GMT  
		Size: 246.0 MB (245952441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf818bfbd63010b013834ec47da74e396b1251b8b683c4e1b5ea47923df84070`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 9.1 KB (9130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:e06f9147ba9772ca4731dfcd218eef782886558631cb16b4fb038e3ccf9391c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11898427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c2d3f915da1ee5ca5d36d89a677228a24b0bc30a0fb316c0d669573730e0de`

```dockerfile
```

-	Layers:
	-	`sha256:c01c53ed3e218067dd499756ff3f3622d1825080c2f239f03dc6385d23f80a65`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 11.9 MB (11886716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f626a3dcae723542bbb7474bba9ee161f4bcd4553aea29c849254942315aa90`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260315.0.500537`

```console
$ docker pull archlinux@sha256:87c122fd99e648dc1a12536d181d40bd7a27ad3201c4bcfa55ccf219b42f4806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260315.0.500537` - linux; amd64

```console
$ docker pull archlinux@sha256:45fe50716152d2b7b43c3a781a2e4c428fd3005baa44b0c4caa59a5fa5dc050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245961571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f26d654f62f77eb5ff99540cddcfdaeeaa8fac2bfc0b97f2fad93e148a2475`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:43:29 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:43:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:43:35 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:43:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3485bafd682693abf8d3d75ec09212f3e00add355d8f933af56e0604c74bf8b7`  
		Last Modified: Mon, 16 Mar 2026 16:44:16 GMT  
		Size: 246.0 MB (245952441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf818bfbd63010b013834ec47da74e396b1251b8b683c4e1b5ea47923df84070`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 9.1 KB (9130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260315.0.500537` - unknown; unknown

```console
$ docker pull archlinux@sha256:e06f9147ba9772ca4731dfcd218eef782886558631cb16b4fb038e3ccf9391c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11898427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c2d3f915da1ee5ca5d36d89a677228a24b0bc30a0fb316c0d669573730e0de`

```dockerfile
```

-	Layers:
	-	`sha256:c01c53ed3e218067dd499756ff3f3622d1825080c2f239f03dc6385d23f80a65`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 11.9 MB (11886716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f626a3dcae723542bbb7474bba9ee161f4bcd4553aea29c849254942315aa90`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:70aace0bf67d14280ca54bc2c7ee15c5fff62684131b34ab38f99f730b643733
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:8c825387fab3f1f20502e4480e3c81c2455615e5fab7fc53a7d693f528cc443f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128325692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05596ed38debe7bb76b70bd7cac20812683948c81fa54aca06e4b1cac83496dc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:42:14 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:42:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:42:17 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:42:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:42:17 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2317a1c19ffbba80187e7b5124537a6007649864a07d2f77a5346055a49966bc`  
		Last Modified: Mon, 16 Mar 2026 16:42:43 GMT  
		Size: 128.3 MB (128317108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f579859357ed6e23f35449a1e7e0afd4140ac522c79637d1cb140414dc8717`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 8.6 KB (8584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d7846d82033aee8945041d7aa0e81884777878a29b9cc15ef063a8f8bd07ae49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8116305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef45d46f67f423d881d1b2096dc15fdd3f84d2ca7702eb1ffc14b4a5567cd49`

```dockerfile
```

-	Layers:
	-	`sha256:10e9b9e7d67c83c472d1bcb62f1b95c124fec9ac5684f7da313c5c3b92835b44`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 8.1 MB (8104376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283dcc06773771146ab6cc8885a308844c6b6559a343c09c15a00e45e5860eb4`  
		Last Modified: Mon, 16 Mar 2026 16:42:40 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9f93fc410174cc8c461a733d5e84c636953e0cace5e26fb703a2bac4dc20883b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:1723ca2122ed3d1fe388bd48d6cd6071e26c18fb83b98c145c87ec16250ef43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268113548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1f6f26373a20f5464d36ea04b76637aa92df15f290c4f6d0e6c9ed39abfcb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:43:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:43:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:43:20 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:43:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9585199d402ed4a8daa2621af9bef196ee78246c0b82a569389353b29e3d6d47`  
		Last Modified: Mon, 16 Mar 2026 16:44:19 GMT  
		Size: 268.1 MB (268103225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ec90be4bc540148d43ef202747b0d81081c54c38cdb6b7da7dc282014e2bee`  
		Last Modified: Mon, 16 Mar 2026 16:44:05 GMT  
		Size: 10.3 KB (10323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:310a3ecfde65c5d865304617198204fdf01810c5278521cd742e05518a62dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12168354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9feb30b550b19b8feb3609d52cbeba7ddb0f6f576c10f34bb9a0b951e7d1b9`

```dockerfile
```

-	Layers:
	-	`sha256:3a23b6f972d8163e5c2a602d9635ffb4d3e7411524be03f82d66c4711387768f`  
		Last Modified: Mon, 16 Mar 2026 16:44:06 GMT  
		Size: 12.2 MB (12156586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90cd3a4741716d55f07ee42cbc4f25640ec9a74d4fccbef2f4ca77cb688a414`  
		Last Modified: Mon, 16 Mar 2026 16:44:05 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260315.0.500537`

```console
$ docker pull archlinux@sha256:9f93fc410174cc8c461a733d5e84c636953e0cace5e26fb703a2bac4dc20883b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260315.0.500537` - linux; amd64

```console
$ docker pull archlinux@sha256:1723ca2122ed3d1fe388bd48d6cd6071e26c18fb83b98c145c87ec16250ef43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268113548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1f6f26373a20f5464d36ea04b76637aa92df15f290c4f6d0e6c9ed39abfcb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:43:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:43:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:43:20 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:43:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9585199d402ed4a8daa2621af9bef196ee78246c0b82a569389353b29e3d6d47`  
		Last Modified: Mon, 16 Mar 2026 16:44:19 GMT  
		Size: 268.1 MB (268103225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ec90be4bc540148d43ef202747b0d81081c54c38cdb6b7da7dc282014e2bee`  
		Last Modified: Mon, 16 Mar 2026 16:44:05 GMT  
		Size: 10.3 KB (10323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260315.0.500537` - unknown; unknown

```console
$ docker pull archlinux@sha256:310a3ecfde65c5d865304617198204fdf01810c5278521cd742e05518a62dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12168354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9feb30b550b19b8feb3609d52cbeba7ddb0f6f576c10f34bb9a0b951e7d1b9`

```dockerfile
```

-	Layers:
	-	`sha256:3a23b6f972d8163e5c2a602d9635ffb4d3e7411524be03f82d66c4711387768f`  
		Last Modified: Mon, 16 Mar 2026 16:44:06 GMT  
		Size: 12.2 MB (12156586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90cd3a4741716d55f07ee42cbc4f25640ec9a74d4fccbef2f4ca77cb688a414`  
		Last Modified: Mon, 16 Mar 2026 16:44:05 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
