<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250202.0.304438`](#archlinuxbase-202502020304438)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250202.0.304438`](#archlinuxbase-devel-202502020304438)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250202.0.304438`](#archlinuxmultilib-devel-202502020304438)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:8b0a7d7e22c2e78539406a37ba2a1eb431d31981be3d76e076f517d3b62204d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:3bce2f83a6504ada72797778a769ba8d3d1dfc22f529c80ef8ba73906033ac26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157486191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b4b47ea315e849e965183f7691a33ebd5b2a9a16a3bca677463ac8087b32ba`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250126.0.301347
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-01-26T00:07:29+00:00
# Sun, 26 Jan 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250126.0.301347' /etc/os-release # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 26 Jan 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:67ec0c022815565d7434df4949e91e31f0de221cfd5be60326bd3df4048bf885`  
		Last Modified: Tue, 28 Jan 2025 01:28:38 GMT  
		Size: 157.5 MB (157477900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28369bbf0fedeaf566c85ca85f3b563ef91d294baec32cce66238189f7a7c91d`  
		Last Modified: Tue, 28 Jan 2025 01:28:34 GMT  
		Size: 8.3 KB (8291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:760d0e0ea4677a55c379f3978d7599763f695d4471e5f76cd61ece5408ee8a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cf857683f5d5bc17410b01b44c329d67b4aaf4caa929c1b8cfe201125897c7`

```dockerfile
```

-	Layers:
	-	`sha256:895a89443e98e48f33777a14ad0535ac71ca23f4acc0ec76f4286c9ee3e8a136`  
		Last Modified: Tue, 28 Jan 2025 01:28:35 GMT  
		Size: 8.1 MB (8088477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d732f7d3e033908e0b5cf56e98fc940200efeff41c24b93395b184124b79ae28`  
		Last Modified: Tue, 28 Jan 2025 01:28:34 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250202.0.304438`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:be024e3a05d303481657494b132e01c42e77a3107efb50721987ecd99607c39a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5568187995f280bc9b2921d93c6ad5bdc21f952954503f856545d70fd9be5b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278598527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e496c7d8a96d7b4722aa0915df9587b1c18c8f5b0c82b436deb74342618a38`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250126.0.301347
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-01-26T00:07:29+00:00
# Sun, 26 Jan 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250126.0.301347' /etc/os-release # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 26 Jan 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:66c3f9f4aca38a7dc9f922fd26e5b25a2fced66440d16b5e53dd7977f060ea8c`  
		Last Modified: Tue, 28 Jan 2025 01:29:11 GMT  
		Size: 278.6 MB (278589485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab05d2bad4390199982294dfcf060c3c4c342920d89dde4bf2c90cef5fa8ea6`  
		Last Modified: Tue, 28 Jan 2025 01:29:03 GMT  
		Size: 9.0 KB (9042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:831e1537f2ed05e7713702bd7cff82e82297211253cdaac9376d22f27f084200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6941f61c4c50cd650a3663c2abd9300ecc1af38cec724bcb4c54031a78fc9ed9`

```dockerfile
```

-	Layers:
	-	`sha256:abdc23c032398cada3a2dbf731b06c6ebf4602be6bd045cffa94ef66999f2bfc`  
		Last Modified: Tue, 28 Jan 2025 01:29:03 GMT  
		Size: 11.9 MB (11895966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7166ce82987a43701efe745e408d3ffba582f6c222f8f61afccb91e5a55308d0`  
		Last Modified: Tue, 28 Jan 2025 01:29:03 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250202.0.304438`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:8b0a7d7e22c2e78539406a37ba2a1eb431d31981be3d76e076f517d3b62204d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:3bce2f83a6504ada72797778a769ba8d3d1dfc22f529c80ef8ba73906033ac26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157486191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b4b47ea315e849e965183f7691a33ebd5b2a9a16a3bca677463ac8087b32ba`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250126.0.301347
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-01-26T00:07:29+00:00
# Sun, 26 Jan 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250126.0.301347' /etc/os-release # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 26 Jan 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:67ec0c022815565d7434df4949e91e31f0de221cfd5be60326bd3df4048bf885`  
		Last Modified: Tue, 28 Jan 2025 01:28:38 GMT  
		Size: 157.5 MB (157477900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28369bbf0fedeaf566c85ca85f3b563ef91d294baec32cce66238189f7a7c91d`  
		Last Modified: Tue, 28 Jan 2025 01:28:34 GMT  
		Size: 8.3 KB (8291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:760d0e0ea4677a55c379f3978d7599763f695d4471e5f76cd61ece5408ee8a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cf857683f5d5bc17410b01b44c329d67b4aaf4caa929c1b8cfe201125897c7`

```dockerfile
```

-	Layers:
	-	`sha256:895a89443e98e48f33777a14ad0535ac71ca23f4acc0ec76f4286c9ee3e8a136`  
		Last Modified: Tue, 28 Jan 2025 01:28:35 GMT  
		Size: 8.1 MB (8088477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d732f7d3e033908e0b5cf56e98fc940200efeff41c24b93395b184124b79ae28`  
		Last Modified: Tue, 28 Jan 2025 01:28:34 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:6a6ed840566e5a6f0ae94a0ce81f0b0885aea54cabd5cf3383b3e2d41744ac30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ba2faadfd27d4dc3835ce585240e0f61b24c0347024fc381ef63f49d4a5370a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328458128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da3b92cbdf48e6bd8e0e1327994a7eeed4691d633598a3b9622518cece59626`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250126.0.301347
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-01-26T00:07:29+00:00
# Sun, 26 Jan 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250126.0.301347' /etc/os-release # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 26 Jan 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c0cb1c42aed3f18ffffa74aa3110b16b2521df6a774df4fae59723b41af39564`  
		Last Modified: Tue, 28 Jan 2025 01:29:05 GMT  
		Size: 328.4 MB (328447889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118b2175bf5367c509c7e2493b81f4717b24f8959859ceb3b93ef1e574faba4`  
		Last Modified: Tue, 28 Jan 2025 01:29:01 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:6591c7430bc90b971b71db2058b6ea3370669151f36b7e19fa98a56eb9dce7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c41a172bbdce816661967c7773378b8fd4edad74e4a1ce17329245f02d1558`

```dockerfile
```

-	Layers:
	-	`sha256:8d110d462a67c4970847158d6e37d2a66b7ae6e8f784ae97f2a052d77bd29cd6`  
		Last Modified: Tue, 28 Jan 2025 01:29:01 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289b3359781f1e395184a1f08a761c9bd6867811dbb07f19f4c211c981cf639f`  
		Last Modified: Tue, 28 Jan 2025 01:29:01 GMT  
		Size: 11.8 KB (11809 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250202.0.304438`

**does not exist** (yet?)
