<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260322.0.504324`](#archlinuxbase-202603220504324)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260322.0.504324`](#archlinuxbase-devel-202603220504324)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260322.0.504324`](#archlinuxmultilib-devel-202603220504324)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:8435d30c1462f94345c3894ebbeaeecd658fcb284aa41b0bcc5f88728933447f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:83b1af810c0cfa8988c8b24182fe94133d70556ffa403346805bd215710d0606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128655969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517df97042928e89b275e4a82ff5e9e02da40de7f907a9a48fffbe0c8cf48ef8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:49:35 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:49:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:49:38 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:49:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b2a51ac4ae494d65c9d18a4636bf2ed832357b4669fa8b7535b8206eebf4ac4a`  
		Last Modified: Mon, 23 Mar 2026 16:50:04 GMT  
		Size: 128.6 MB (128647387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f007d0715520786a0e9020c41387ba39ef23a87fec7b8ba69de50ef698f4985b`  
		Last Modified: Mon, 23 Mar 2026 16:50:01 GMT  
		Size: 8.6 KB (8582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:2821960a6bd099cf83a33bd38e36ab749088614915c51d5b926a1288561a7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dac44cf26742c29789ee6eab2c60bca4867a1e6323e0f8f9549cec0e0c94af`

```dockerfile
```

-	Layers:
	-	`sha256:96d574a8c3974d4f1815426b771c01f3a8a8902592285ee2e0d0bacdf20fea6e`  
		Last Modified: Mon, 23 Mar 2026 16:50:01 GMT  
		Size: 8.1 MB (8143653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d80fa1c38334bed03992d6709cca23afd53504c0e683174a9265840096ec62c5`  
		Last Modified: Mon, 23 Mar 2026 16:50:00 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260322.0.504324`

```console
$ docker pull archlinux@sha256:8435d30c1462f94345c3894ebbeaeecd658fcb284aa41b0bcc5f88728933447f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260322.0.504324` - linux; amd64

```console
$ docker pull archlinux@sha256:83b1af810c0cfa8988c8b24182fe94133d70556ffa403346805bd215710d0606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128655969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517df97042928e89b275e4a82ff5e9e02da40de7f907a9a48fffbe0c8cf48ef8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:49:35 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:49:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:49:38 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:49:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b2a51ac4ae494d65c9d18a4636bf2ed832357b4669fa8b7535b8206eebf4ac4a`  
		Last Modified: Mon, 23 Mar 2026 16:50:04 GMT  
		Size: 128.6 MB (128647387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f007d0715520786a0e9020c41387ba39ef23a87fec7b8ba69de50ef698f4985b`  
		Last Modified: Mon, 23 Mar 2026 16:50:01 GMT  
		Size: 8.6 KB (8582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260322.0.504324` - unknown; unknown

```console
$ docker pull archlinux@sha256:2821960a6bd099cf83a33bd38e36ab749088614915c51d5b926a1288561a7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dac44cf26742c29789ee6eab2c60bca4867a1e6323e0f8f9549cec0e0c94af`

```dockerfile
```

-	Layers:
	-	`sha256:96d574a8c3974d4f1815426b771c01f3a8a8902592285ee2e0d0bacdf20fea6e`  
		Last Modified: Mon, 23 Mar 2026 16:50:01 GMT  
		Size: 8.1 MB (8143653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d80fa1c38334bed03992d6709cca23afd53504c0e683174a9265840096ec62c5`  
		Last Modified: Mon, 23 Mar 2026 16:50:00 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:233f52197321141f63c1d389284c868101dc94ef8f46ac31b908e3e4b6ea7cb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:351ef3518e944780972d651e6961d69d050350c31fcc973c9b463fa8665988f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246275217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace0273710d59d9137247f8c89c3763796cbde392da16cb0b8e2bbb49bdb59fc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:51:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:51:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:51:11 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:51:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:361908d86bc2bc504d2c2942eecfbc836824e2e38e2799388d65ed96f7dfd4d7`  
		Last Modified: Mon, 23 Mar 2026 16:51:58 GMT  
		Size: 246.3 MB (246266088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4126aa50fdb3f9d29dfb3d546b11b936a4dbbc548dd815ece5e7e4a43bb92b`  
		Last Modified: Mon, 23 Mar 2026 16:51:52 GMT  
		Size: 9.1 KB (9129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:e61294dc413506b17260eeac9efb6e4c352292316f92e960534e1b8d367ac22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11938961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0eca649dafb6c72883aeab81116d7b9c2106d2f4e94b403141147dc4742316`

```dockerfile
```

-	Layers:
	-	`sha256:f2b5bcb6da6d99a4e998446b5cee23b8b28a8d57776e312faa5311d6689acae4`  
		Last Modified: Mon, 23 Mar 2026 16:51:53 GMT  
		Size: 11.9 MB (11927250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67bb9328e839ec28cbb18f5911cdfdd8f481f547c7eea494f43c32ac389529a`  
		Last Modified: Mon, 23 Mar 2026 16:51:52 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260322.0.504324`

```console
$ docker pull archlinux@sha256:233f52197321141f63c1d389284c868101dc94ef8f46ac31b908e3e4b6ea7cb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260322.0.504324` - linux; amd64

```console
$ docker pull archlinux@sha256:351ef3518e944780972d651e6961d69d050350c31fcc973c9b463fa8665988f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246275217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace0273710d59d9137247f8c89c3763796cbde392da16cb0b8e2bbb49bdb59fc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:51:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:51:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:51:11 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:51:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:361908d86bc2bc504d2c2942eecfbc836824e2e38e2799388d65ed96f7dfd4d7`  
		Last Modified: Mon, 23 Mar 2026 16:51:58 GMT  
		Size: 246.3 MB (246266088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4126aa50fdb3f9d29dfb3d546b11b936a4dbbc548dd815ece5e7e4a43bb92b`  
		Last Modified: Mon, 23 Mar 2026 16:51:52 GMT  
		Size: 9.1 KB (9129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260322.0.504324` - unknown; unknown

```console
$ docker pull archlinux@sha256:e61294dc413506b17260eeac9efb6e4c352292316f92e960534e1b8d367ac22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11938961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0eca649dafb6c72883aeab81116d7b9c2106d2f4e94b403141147dc4742316`

```dockerfile
```

-	Layers:
	-	`sha256:f2b5bcb6da6d99a4e998446b5cee23b8b28a8d57776e312faa5311d6689acae4`  
		Last Modified: Mon, 23 Mar 2026 16:51:53 GMT  
		Size: 11.9 MB (11927250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67bb9328e839ec28cbb18f5911cdfdd8f481f547c7eea494f43c32ac389529a`  
		Last Modified: Mon, 23 Mar 2026 16:51:52 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:8435d30c1462f94345c3894ebbeaeecd658fcb284aa41b0bcc5f88728933447f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:83b1af810c0cfa8988c8b24182fe94133d70556ffa403346805bd215710d0606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128655969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517df97042928e89b275e4a82ff5e9e02da40de7f907a9a48fffbe0c8cf48ef8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:49:35 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:49:35 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:49:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:49:38 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:49:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b2a51ac4ae494d65c9d18a4636bf2ed832357b4669fa8b7535b8206eebf4ac4a`  
		Last Modified: Mon, 23 Mar 2026 16:50:04 GMT  
		Size: 128.6 MB (128647387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f007d0715520786a0e9020c41387ba39ef23a87fec7b8ba69de50ef698f4985b`  
		Last Modified: Mon, 23 Mar 2026 16:50:01 GMT  
		Size: 8.6 KB (8582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:2821960a6bd099cf83a33bd38e36ab749088614915c51d5b926a1288561a7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dac44cf26742c29789ee6eab2c60bca4867a1e6323e0f8f9549cec0e0c94af`

```dockerfile
```

-	Layers:
	-	`sha256:96d574a8c3974d4f1815426b771c01f3a8a8902592285ee2e0d0bacdf20fea6e`  
		Last Modified: Mon, 23 Mar 2026 16:50:01 GMT  
		Size: 8.1 MB (8143653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d80fa1c38334bed03992d6709cca23afd53504c0e683174a9265840096ec62c5`  
		Last Modified: Mon, 23 Mar 2026 16:50:00 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:8d0ae41cc3261c424b4a00af0982a9ca35257740b3a23ae5bda2ceb7212467aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ac3f08986561daddd69300793660bddebf3f795fe5de725715f29afe9c506724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268448104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca969d1167bf24ce7f3aad6a3daa62918b454f4b768a7a2d8db427e4c7024743`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:50:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:50:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:50:42 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:50:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c52b47f47cd63adb3262045f0c9366d519ea9bab319a612d9eeaf03a37c25b20`  
		Last Modified: Mon, 23 Mar 2026 16:51:33 GMT  
		Size: 268.4 MB (268437781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5926d58339bb1a7c2c7e8042eba02ab1a32dd5f0aba0e54b5a6170eb39bfe61e`  
		Last Modified: Mon, 23 Mar 2026 16:51:27 GMT  
		Size: 10.3 KB (10323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d2e7c0a66b29c119115044157b1a4500202cd78613d12337ed25e546f548829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12208888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750285c53182f7dafc406384341a17cc15ec699aaf051806beda5b07fb867ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7312f8bc40d7be95914cb3d6db40cd171562471a5e03700dd02183351e76249`  
		Last Modified: Mon, 23 Mar 2026 16:51:28 GMT  
		Size: 12.2 MB (12197120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a37ab2fadaed5446beeccf7ca85c53fc1ac1600177cdb40abbe5951c72c8d212`  
		Last Modified: Mon, 23 Mar 2026 16:51:28 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260322.0.504324`

```console
$ docker pull archlinux@sha256:8d0ae41cc3261c424b4a00af0982a9ca35257740b3a23ae5bda2ceb7212467aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260322.0.504324` - linux; amd64

```console
$ docker pull archlinux@sha256:ac3f08986561daddd69300793660bddebf3f795fe5de725715f29afe9c506724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268448104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca969d1167bf24ce7f3aad6a3daa62918b454f4b768a7a2d8db427e4c7024743`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:50:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:50:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:50:42 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:50:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c52b47f47cd63adb3262045f0c9366d519ea9bab319a612d9eeaf03a37c25b20`  
		Last Modified: Mon, 23 Mar 2026 16:51:33 GMT  
		Size: 268.4 MB (268437781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5926d58339bb1a7c2c7e8042eba02ab1a32dd5f0aba0e54b5a6170eb39bfe61e`  
		Last Modified: Mon, 23 Mar 2026 16:51:27 GMT  
		Size: 10.3 KB (10323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260322.0.504324` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d2e7c0a66b29c119115044157b1a4500202cd78613d12337ed25e546f548829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12208888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750285c53182f7dafc406384341a17cc15ec699aaf051806beda5b07fb867ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7312f8bc40d7be95914cb3d6db40cd171562471a5e03700dd02183351e76249`  
		Last Modified: Mon, 23 Mar 2026 16:51:28 GMT  
		Size: 12.2 MB (12197120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a37ab2fadaed5446beeccf7ca85c53fc1ac1600177cdb40abbe5951c72c8d212`  
		Last Modified: Mon, 23 Mar 2026 16:51:28 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
