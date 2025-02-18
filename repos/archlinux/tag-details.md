<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250216.0.309127`](#archlinuxbase-202502160309127)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250216.0.309127`](#archlinuxbase-devel-202502160309127)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250216.0.309127`](#archlinuxmultilib-devel-202502160309127)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:33ff44f3d1d18207c1bdc1bf5c4283541b7680bb60e3092e6973437e4e1c3927
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:2a006ed10836e49964826d6b310b169983bffd474917e02727342012f1b970c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157673353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957e6371bf45c26d24c8087e3945b87428edc053e2f9bbdd6dfb730c04cd31df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c4ce51beea9c3c5783dd11628e243d1c6679951a48f0168e07d67ad3ff6c26c7`  
		Last Modified: Mon, 10 Feb 2025 20:48:58 GMT  
		Size: 157.7 MB (157665076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b40c5e7a481307aa7619a8d87e35c219aa4561ba990a0966f3bc9d1a6010a`  
		Last Modified: Fri, 14 Feb 2025 23:48:48 GMT  
		Size: 8.3 KB (8277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:11255ef2bdd57c2286e5d2dc5db45080286b763ac8feb6d5377c86a2e42028be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f360b3630fdc7343d3d479d626edf4d0194ad46a4416718d7ebbe1cdd18db038`

```dockerfile
```

-	Layers:
	-	`sha256:07222cb7abfdd97a79eed85c16598f4c62e302a850f356cc607f4206f8a79d8c`  
		Last Modified: Fri, 14 Feb 2025 23:48:15 GMT  
		Size: 8.1 MB (8089059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd7a88f9cd0c9337150a73888c196eb9d6b87b2ceb65bd05a8ab52ac11fa19e`  
		Last Modified: Fri, 14 Feb 2025 23:48:15 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250216.0.309127`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:2e64be3bcaeb69bff00ba401cce9b26277ca29ac3f4ef661f3a31d803e96a58f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e5c8d0ccd853f86c2eaa3148cd4c51062229014d80f1c8efed99993c3ed00eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278801075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261975b3eff42077ac4c418afc8197ae290e843228e6cdda4875ec84c84bb29b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:597f8ce19d766bcdf33ec6a6ec4f60bc434037a9a9efc05adab134ffa7dd739a`  
		Last Modified: Mon, 10 Feb 2025 20:50:42 GMT  
		Size: 278.8 MB (278792008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33041fa63b5c1f16df393202a8baafc5957fd71dc5714f2cf458084031584a25`  
		Last Modified: Fri, 14 Feb 2025 23:49:31 GMT  
		Size: 9.1 KB (9067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:18402c1595b399977631d7a471a62f3a338cfea6ef9dda2670e55f79fc00dece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a6b942484670819e0f1c230103efc62d510b64d984eb1d8aeb77c585a8210`

```dockerfile
```

-	Layers:
	-	`sha256:dd1cb379753c056fab3676446e4f6895da435bb22b038213636e3b54e1a04698`  
		Last Modified: Fri, 14 Feb 2025 23:48:23 GMT  
		Size: 11.9 MB (11896538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1543f0e932a83cb097159173b2a84b2e5360ad919c82829cd5e10feb7495db4`  
		Last Modified: Fri, 14 Feb 2025 23:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250216.0.309127`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:33ff44f3d1d18207c1bdc1bf5c4283541b7680bb60e3092e6973437e4e1c3927
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2a006ed10836e49964826d6b310b169983bffd474917e02727342012f1b970c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157673353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957e6371bf45c26d24c8087e3945b87428edc053e2f9bbdd6dfb730c04cd31df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c4ce51beea9c3c5783dd11628e243d1c6679951a48f0168e07d67ad3ff6c26c7`  
		Last Modified: Mon, 10 Feb 2025 20:48:58 GMT  
		Size: 157.7 MB (157665076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b40c5e7a481307aa7619a8d87e35c219aa4561ba990a0966f3bc9d1a6010a`  
		Last Modified: Fri, 14 Feb 2025 23:48:48 GMT  
		Size: 8.3 KB (8277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:11255ef2bdd57c2286e5d2dc5db45080286b763ac8feb6d5377c86a2e42028be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f360b3630fdc7343d3d479d626edf4d0194ad46a4416718d7ebbe1cdd18db038`

```dockerfile
```

-	Layers:
	-	`sha256:07222cb7abfdd97a79eed85c16598f4c62e302a850f356cc607f4206f8a79d8c`  
		Last Modified: Fri, 14 Feb 2025 23:48:15 GMT  
		Size: 8.1 MB (8089059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd7a88f9cd0c9337150a73888c196eb9d6b87b2ceb65bd05a8ab52ac11fa19e`  
		Last Modified: Fri, 14 Feb 2025 23:48:15 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:bdb4a8d2bb14339e2c8d782da829b411f2bf04f328c521730f765291799195d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8ff14dbb10ae1f83d829a38e17b67418a08924876e686add1da9bb14f749aaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51df7133cb3743c40ebd4defe13a570da07fbfa0fc243ca6fd2235fcb0868af`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:61c8fceafc7f0cdee9f810aaad8a75bd636d2b072b8452854e73c7c6f001b2c0`  
		Last Modified: Mon, 10 Feb 2025 21:05:30 GMT  
		Size: 328.8 MB (328805658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a65587c9714ca6ad5a8e17b56eafc9d96e8f8dc887fd8dd8bdaff6458093e02`  
		Last Modified: Sat, 15 Feb 2025 00:06:34 GMT  
		Size: 10.2 KB (10219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:6d844b9620d501968ea96f0e065f8414a6081ce89b35694587139121b1843266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7e95d548c3ee53012b53084e22590c7c706efe4e92c82adc088d3cf5e6a53f`

```dockerfile
```

-	Layers:
	-	`sha256:38747e51b379c4bf7f793ca3cf267721bf9dd50f7749e8313eb31e8d2390d655`  
		Last Modified: Fri, 14 Feb 2025 23:48:23 GMT  
		Size: 12.2 MB (12165053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20d15760832cc19f95649693a569c324d37db3c647121e7791593ebac964f17`  
		Last Modified: Fri, 14 Feb 2025 23:48:23 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250216.0.309127`

**does not exist** (yet?)
