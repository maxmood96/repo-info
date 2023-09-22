<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20230921.0.180222`](#archlinuxbase-202309210180222)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20230921.0.180222`](#archlinuxbase-devel-202309210180222)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:e2a0061c92706e059fdd33a2c6e04e4d02019b989812f6a5b34d7f3703e9300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:414f7fbcd3a60c711c5c29faaa207bd5edf9a1417cb2414618b41c59d951e2c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147783072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74269d97bbd7b77b309d2098bef0cc097db369ad978191b3dcc23655c1efc9ea`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.version=20230921.0.180222
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.revision=c432cbcbe27301dd9b2f4e1300b5ca0ff875e1ca
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.created=2023-09-21T04:21:54+00:00
# Thu, 21 Sep 2023 23:20:13 GMT
COPY dir:cee041fe16b97b5555fe3fe57d04d0b2a66c9227635e16cec4fa4b03f81bab25 in / 
# Thu, 21 Sep 2023 23:20:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230921.0.180222' /etc/os-release
# Thu, 21 Sep 2023 23:20:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Sep 2023 23:20:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4bb294212b48940bb01dc682ee03b297ab9b28603e1e64e31684eea47ae6b44a`  
		Last Modified: Thu, 21 Sep 2023 23:21:56 GMT  
		Size: 147.8 MB (147774945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f5a258dd4fe7453e2163ab0fcebaffa7ff4775ebcda31f075ff84e6ac8d511`  
		Last Modified: Thu, 21 Sep 2023 23:21:36 GMT  
		Size: 8.1 KB (8127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20230921.0.180222`

```console
$ docker pull archlinux@sha256:e2a0061c92706e059fdd33a2c6e04e4d02019b989812f6a5b34d7f3703e9300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20230921.0.180222` - linux; amd64

```console
$ docker pull archlinux@sha256:414f7fbcd3a60c711c5c29faaa207bd5edf9a1417cb2414618b41c59d951e2c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147783072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74269d97bbd7b77b309d2098bef0cc097db369ad978191b3dcc23655c1efc9ea`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.version=20230921.0.180222
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.revision=c432cbcbe27301dd9b2f4e1300b5ca0ff875e1ca
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.created=2023-09-21T04:21:54+00:00
# Thu, 21 Sep 2023 23:20:13 GMT
COPY dir:cee041fe16b97b5555fe3fe57d04d0b2a66c9227635e16cec4fa4b03f81bab25 in / 
# Thu, 21 Sep 2023 23:20:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230921.0.180222' /etc/os-release
# Thu, 21 Sep 2023 23:20:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Sep 2023 23:20:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4bb294212b48940bb01dc682ee03b297ab9b28603e1e64e31684eea47ae6b44a`  
		Last Modified: Thu, 21 Sep 2023 23:21:56 GMT  
		Size: 147.8 MB (147774945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f5a258dd4fe7453e2163ab0fcebaffa7ff4775ebcda31f075ff84e6ac8d511`  
		Last Modified: Thu, 21 Sep 2023 23:21:36 GMT  
		Size: 8.1 KB (8127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:bf5c44307643441db1a7646017c4f673476488a663e3ef196afcfdca20bd38b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:781932307cf0d6ef99f92e03584498971d028cc0ec6828e77c6fd3a7dd819384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265829206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801b498cd83a43c68bf029d5a2fe6edacaf6c9ff9f75660f54e2c2dd9b823924`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.version=20230921.0.180222
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.revision=c432cbcbe27301dd9b2f4e1300b5ca0ff875e1ca
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.created=2023-09-21T04:21:57+00:00
# Thu, 21 Sep 2023 23:21:17 GMT
COPY dir:54b78287ff1869fd2434a586fb08252b6683ddb826baafe37e7dbd6674f5626d in / 
# Thu, 21 Sep 2023 23:21:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230921.0.180222' /etc/os-release
# Thu, 21 Sep 2023 23:21:20 GMT
ENV LANG=C.UTF-8
# Thu, 21 Sep 2023 23:21:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:22c1a814f5a46ebf6beeb730dfd23c0c6ae36f4284c4c394f1aa3c9855f2c7ed`  
		Last Modified: Thu, 21 Sep 2023 23:22:43 GMT  
		Size: 265.8 MB (265820308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc5d45db49a8b45c72a8a11242628ec79b4b5045d1c07e5a958203ea6c4907a`  
		Last Modified: Thu, 21 Sep 2023 23:22:07 GMT  
		Size: 8.9 KB (8898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20230921.0.180222`

```console
$ docker pull archlinux@sha256:bf5c44307643441db1a7646017c4f673476488a663e3ef196afcfdca20bd38b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230921.0.180222` - linux; amd64

```console
$ docker pull archlinux@sha256:781932307cf0d6ef99f92e03584498971d028cc0ec6828e77c6fd3a7dd819384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265829206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801b498cd83a43c68bf029d5a2fe6edacaf6c9ff9f75660f54e2c2dd9b823924`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.version=20230921.0.180222
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.revision=c432cbcbe27301dd9b2f4e1300b5ca0ff875e1ca
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.created=2023-09-21T04:21:57+00:00
# Thu, 21 Sep 2023 23:21:17 GMT
COPY dir:54b78287ff1869fd2434a586fb08252b6683ddb826baafe37e7dbd6674f5626d in / 
# Thu, 21 Sep 2023 23:21:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230921.0.180222' /etc/os-release
# Thu, 21 Sep 2023 23:21:20 GMT
ENV LANG=C.UTF-8
# Thu, 21 Sep 2023 23:21:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:22c1a814f5a46ebf6beeb730dfd23c0c6ae36f4284c4c394f1aa3c9855f2c7ed`  
		Last Modified: Thu, 21 Sep 2023 23:22:43 GMT  
		Size: 265.8 MB (265820308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc5d45db49a8b45c72a8a11242628ec79b4b5045d1c07e5a958203ea6c4907a`  
		Last Modified: Thu, 21 Sep 2023 23:22:07 GMT  
		Size: 8.9 KB (8898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:e2a0061c92706e059fdd33a2c6e04e4d02019b989812f6a5b34d7f3703e9300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:414f7fbcd3a60c711c5c29faaa207bd5edf9a1417cb2414618b41c59d951e2c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147783072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74269d97bbd7b77b309d2098bef0cc097db369ad978191b3dcc23655c1efc9ea`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.version=20230921.0.180222
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.revision=c432cbcbe27301dd9b2f4e1300b5ca0ff875e1ca
# Thu, 21 Sep 2023 23:20:07 GMT
LABEL org.opencontainers.image.created=2023-09-21T04:21:54+00:00
# Thu, 21 Sep 2023 23:20:13 GMT
COPY dir:cee041fe16b97b5555fe3fe57d04d0b2a66c9227635e16cec4fa4b03f81bab25 in / 
# Thu, 21 Sep 2023 23:20:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230921.0.180222' /etc/os-release
# Thu, 21 Sep 2023 23:20:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Sep 2023 23:20:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4bb294212b48940bb01dc682ee03b297ab9b28603e1e64e31684eea47ae6b44a`  
		Last Modified: Thu, 21 Sep 2023 23:21:56 GMT  
		Size: 147.8 MB (147774945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f5a258dd4fe7453e2163ab0fcebaffa7ff4775ebcda31f075ff84e6ac8d511`  
		Last Modified: Thu, 21 Sep 2023 23:21:36 GMT  
		Size: 8.1 KB (8127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
