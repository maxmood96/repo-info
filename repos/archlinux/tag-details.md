<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240101.0.204074`](#archlinuxbase-202401010204074)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240101.0.204074`](#archlinuxbase-devel-202401010204074)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240101.0.204074`](#archlinuxmultilib-devel-202401010204074)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:2dbd72d1e5510e047db7f441bf9069e9c53391b87e04e5bee3f379cd03cec060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:85dc960fa1b01560091e6de62b09c4ad99c35cf818f6a7e2b2118a57f712bcb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147996205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cda8061254a9e2a6c1b57275e0c71174788b3775346fa3511d67163ad90be34`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:08:22 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sat, 16 Mar 2024 06:08:22 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:08:29 GMT
COPY dir:500a387e180f5288f7f6cc8c9e7245548b04a53ce9c569583f3e160673182bf9 in / 
# Sat, 16 Mar 2024 06:08:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:08:31 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:08:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a82a64c3a8439c75d8e584181427b073712afd1454747bec3dcb84bcbe19ac5`  
		Last Modified: Mon, 01 Jan 2024 19:19:12 GMT  
		Size: 148.0 MB (147988087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a73115b61227673ac6c1a8802a4b3d939967a9efef31fee246a3acd790895`  
		Last Modified: Sat, 16 Mar 2024 06:11:15 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20240101.0.204074`

```console
$ docker pull archlinux@sha256:2dbd72d1e5510e047db7f441bf9069e9c53391b87e04e5bee3f379cd03cec060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:85dc960fa1b01560091e6de62b09c4ad99c35cf818f6a7e2b2118a57f712bcb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147996205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cda8061254a9e2a6c1b57275e0c71174788b3775346fa3511d67163ad90be34`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:08:22 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sat, 16 Mar 2024 06:08:22 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:08:29 GMT
COPY dir:500a387e180f5288f7f6cc8c9e7245548b04a53ce9c569583f3e160673182bf9 in / 
# Sat, 16 Mar 2024 06:08:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:08:31 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:08:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a82a64c3a8439c75d8e584181427b073712afd1454747bec3dcb84bcbe19ac5`  
		Last Modified: Mon, 01 Jan 2024 19:19:12 GMT  
		Size: 148.0 MB (147988087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a73115b61227673ac6c1a8802a4b3d939967a9efef31fee246a3acd790895`  
		Last Modified: Sat, 16 Mar 2024 06:11:15 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:10ce20a6f7e0844e2b0cbe367dc32b584dfbfa9dc068712d119b192c5c83b637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:095d7d25a366555f47926b4ff5b8e2284b671499310ee3b5e270a77b7f3cdffb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b8abb90a6e1b1a62cd58dc9c2e8f1f91ed3fd1820f5dd12e2e80afb6234eaf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:09:31 GMT
COPY dir:26a13fc3a1ba45fe2c4b0785d8b1a68ce5991bc4fbd4c078f8b86bf9c621781e in / 
# Sat, 16 Mar 2024 06:09:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:09:35 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:09:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:444f393ce858c4b3035c5cb5e2e6b5b46661dd73311818d48dead4150ac68209`  
		Last Modified: Mon, 01 Jan 2024 19:20:00 GMT  
		Size: 266.2 MB (266229441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874e70007832dd23b4111f786258826ced23964005f0e37dabb80e2327ed9128`  
		Last Modified: Sat, 16 Mar 2024 06:11:23 GMT  
		Size: 8.9 KB (8936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:10ce20a6f7e0844e2b0cbe367dc32b584dfbfa9dc068712d119b192c5c83b637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:095d7d25a366555f47926b4ff5b8e2284b671499310ee3b5e270a77b7f3cdffb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b8abb90a6e1b1a62cd58dc9c2e8f1f91ed3fd1820f5dd12e2e80afb6234eaf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:09:31 GMT
COPY dir:26a13fc3a1ba45fe2c4b0785d8b1a68ce5991bc4fbd4c078f8b86bf9c621781e in / 
# Sat, 16 Mar 2024 06:09:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:09:35 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:09:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:444f393ce858c4b3035c5cb5e2e6b5b46661dd73311818d48dead4150ac68209`  
		Last Modified: Mon, 01 Jan 2024 19:20:00 GMT  
		Size: 266.2 MB (266229441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874e70007832dd23b4111f786258826ced23964005f0e37dabb80e2327ed9128`  
		Last Modified: Sat, 16 Mar 2024 06:11:23 GMT  
		Size: 8.9 KB (8936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:2dbd72d1e5510e047db7f441bf9069e9c53391b87e04e5bee3f379cd03cec060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:85dc960fa1b01560091e6de62b09c4ad99c35cf818f6a7e2b2118a57f712bcb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147996205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cda8061254a9e2a6c1b57275e0c71174788b3775346fa3511d67163ad90be34`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:08:22 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sat, 16 Mar 2024 06:08:22 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:08:29 GMT
COPY dir:500a387e180f5288f7f6cc8c9e7245548b04a53ce9c569583f3e160673182bf9 in / 
# Sat, 16 Mar 2024 06:08:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:08:31 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:08:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a82a64c3a8439c75d8e584181427b073712afd1454747bec3dcb84bcbe19ac5`  
		Last Modified: Mon, 01 Jan 2024 19:19:12 GMT  
		Size: 148.0 MB (147988087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a73115b61227673ac6c1a8802a4b3d939967a9efef31fee246a3acd790895`  
		Last Modified: Sat, 16 Mar 2024 06:11:15 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:c0dc3c22dc0ee2bc758c62038b4ed5026af98970361b488e68cafa4384d5dccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:bdabdaf70259e439876c7d29ce85b2217be95601544553b8e029c7322e8542e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316045008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9feecb236dcf9e4ae3a84719eea979bd3cdd1b6d184aa492d7304964b8f18861`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:10:51 GMT
COPY dir:75c66889520f549930c0f406d7a42c7d20e2d1d2e662322c69dc3a2dcb5d5bc5 in / 
# Sat, 16 Mar 2024 06:10:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:10:55 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:10:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f377e15cb8d612a50f6c51ebcee45ab2e4b9221e4dc99f177dc54b529f9f0edf`  
		Last Modified: Mon, 01 Jan 2024 19:20:55 GMT  
		Size: 316.0 MB (316034966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc436cc52de3b0668da7c860873c75ff908ba8966eebc758a7c95e6cb0b4b5e`  
		Last Modified: Sat, 16 Mar 2024 06:11:30 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:multilib-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:c0dc3c22dc0ee2bc758c62038b4ed5026af98970361b488e68cafa4384d5dccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:multilib-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:bdabdaf70259e439876c7d29ce85b2217be95601544553b8e029c7322e8542e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316045008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9feecb236dcf9e4ae3a84719eea979bd3cdd1b6d184aa492d7304964b8f18861`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:10:51 GMT
COPY dir:75c66889520f549930c0f406d7a42c7d20e2d1d2e662322c69dc3a2dcb5d5bc5 in / 
# Sat, 16 Mar 2024 06:10:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:10:55 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:10:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f377e15cb8d612a50f6c51ebcee45ab2e4b9221e4dc99f177dc54b529f9f0edf`  
		Last Modified: Mon, 01 Jan 2024 19:20:55 GMT  
		Size: 316.0 MB (316034966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc436cc52de3b0668da7c860873c75ff908ba8966eebc758a7c95e6cb0b4b5e`  
		Last Modified: Sat, 16 Mar 2024 06:11:30 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
