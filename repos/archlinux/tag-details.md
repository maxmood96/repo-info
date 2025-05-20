<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250518.0.352066`](#archlinuxbase-202505180352066)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250518.0.352066`](#archlinuxbase-devel-202505180352066)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250518.0.352066`](#archlinuxmultilib-devel-202505180352066)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:270c346af46e9bd91844bc3dd2407d44ecd109fe6e1d945dfc5b27cdcb97a806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:eac02ca6806885f170493a1928407f4a41ab8dde3398b5b2c92bef4e05250df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162341614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9831665f7a97cc674381a692205ea79d52815a35164fdcaa02a06d82f5bc122`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250511.0.348143
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-05-11T00:07:38+00:00
# Sun, 11 May 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 May 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250511.0.348143' /etc/os-release # buildkit
# Sun, 11 May 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 11 May 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:74566064f022b733c1e5e23d8e3b9d139f94d2fc031bed3e1b4e8766ca1f1090`  
		Last Modified: Tue, 13 May 2025 19:17:39 GMT  
		Size: 162.3 MB (162333265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a06427524f50d6f87a8c7078931273be9f868e6026d38a49f2f738926751b9`  
		Last Modified: Tue, 13 May 2025 19:17:30 GMT  
		Size: 8.3 KB (8349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:9ed64787ebe6ca27b75eee90c0b2a0f7a72a88d04721da33f0cd04636097bd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8177496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9a0ef1007bf9909a5ac24a3a76b72dbb55cf77a271a79d1991ba0443498540`

```dockerfile
```

-	Layers:
	-	`sha256:4fe8a0f81d613db6c8c97ceb012a09cae8fb4dde1e4c26f39ad7bde08ebed7e1`  
		Last Modified: Thu, 15 May 2025 20:28:05 GMT  
		Size: 8.2 MB (8165524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b153857d92db94e23bdcf399d9be91525db2e9f58fc79ed50bf8294ccb9b0ded`  
		Last Modified: Thu, 15 May 2025 20:28:04 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250518.0.352066`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:880766de4e2961c425c6de1666ff852c59e0432fef12cbea7b8c678a80e80710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b9a97634ea0221aa1585a2737234acac0d2af78514c45c33529fd63c965d8807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287038782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905aab36193055ef8dad88ca20da1c3f3e4a4370aa2e807c6415e7a2354e01d3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250511.0.348143
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-05-11T00:07:38+00:00
# Sun, 11 May 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 May 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250511.0.348143' /etc/os-release # buildkit
# Sun, 11 May 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 11 May 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:dfd741f6c2c280c7836df3cd6f21735be091319b1d2cf5ac19cc6cb7ceb6c00e`  
		Last Modified: Tue, 13 May 2025 19:25:50 GMT  
		Size: 287.0 MB (287029581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd4e158398659e624ef7fd8c61e5620b7c82e6733e0653c4eabf1802bbc508e`  
		Last Modified: Tue, 13 May 2025 19:19:10 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0758f567102c007a21be0ef4532239688a67ac23925ba06fe47701faa22cfce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12038073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5970151c2af6f779f309f7b952aa5cd8d63816a9a4a67ee3b259bf43252e8d65`

```dockerfile
```

-	Layers:
	-	`sha256:028f2f8f298389d380d4c47dccb911c42d06e33ce8fefef2abb95428cc47aa97`  
		Last Modified: Fri, 16 May 2025 17:19:13 GMT  
		Size: 12.0 MB (12026319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f362015cdb894c9795483cd12bc58adc2bceed0b0a77c78e6bb4e9ae41832422`  
		Last Modified: Fri, 16 May 2025 17:19:12 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250518.0.352066`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:270c346af46e9bd91844bc3dd2407d44ecd109fe6e1d945dfc5b27cdcb97a806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:eac02ca6806885f170493a1928407f4a41ab8dde3398b5b2c92bef4e05250df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162341614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9831665f7a97cc674381a692205ea79d52815a35164fdcaa02a06d82f5bc122`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250511.0.348143
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-05-11T00:07:38+00:00
# Sun, 11 May 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 May 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250511.0.348143' /etc/os-release # buildkit
# Sun, 11 May 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 11 May 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:74566064f022b733c1e5e23d8e3b9d139f94d2fc031bed3e1b4e8766ca1f1090`  
		Last Modified: Tue, 13 May 2025 19:17:39 GMT  
		Size: 162.3 MB (162333265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a06427524f50d6f87a8c7078931273be9f868e6026d38a49f2f738926751b9`  
		Last Modified: Tue, 13 May 2025 19:17:30 GMT  
		Size: 8.3 KB (8349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:9ed64787ebe6ca27b75eee90c0b2a0f7a72a88d04721da33f0cd04636097bd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8177496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9a0ef1007bf9909a5ac24a3a76b72dbb55cf77a271a79d1991ba0443498540`

```dockerfile
```

-	Layers:
	-	`sha256:4fe8a0f81d613db6c8c97ceb012a09cae8fb4dde1e4c26f39ad7bde08ebed7e1`  
		Last Modified: Thu, 15 May 2025 20:28:05 GMT  
		Size: 8.2 MB (8165524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b153857d92db94e23bdcf399d9be91525db2e9f58fc79ed50bf8294ccb9b0ded`  
		Last Modified: Thu, 15 May 2025 20:28:04 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:8852c489e3b0daf5d8afe1c94b4a4dd8de38176060a5971da3a2776e62609caf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ff718773c826ed5de0b9ec276971255531eaafe903772144c905ec0928aa0ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338205246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0737f8c336251e31c3f954aa4276ac32957996ba981aa300aa816316b45f843e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250511.0.348143
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-05-11T00:07:38+00:00
# Sun, 11 May 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 May 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250511.0.348143' /etc/os-release # buildkit
# Sun, 11 May 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 11 May 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f6d25a390ff1e44723dbbc555061dde908cb77ebce6778723e4ce827eaa6132b`  
		Last Modified: Thu, 15 May 2025 20:17:24 GMT  
		Size: 338.2 MB (338194960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56fade2eeed012139f19a60b32ed1b404bb12638044328c99efb8081ffe0d94`  
		Last Modified: Thu, 15 May 2025 20:17:11 GMT  
		Size: 10.3 KB (10286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:107e8c8821204655b83d8d6cb710a3786868340eb3f2883d1d62e97c6fb125c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12306665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2683507c077fa976fd740e41e31a3b97cda0b7e17cfa1696ba23281bfb92cc7`

```dockerfile
```

-	Layers:
	-	`sha256:8257bc2a4074a74246e47fd6cfde70c992860d0cac6e619ef012b660dadf90f6`  
		Last Modified: Mon, 12 May 2025 19:09:44 GMT  
		Size: 12.3 MB (12294854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd54c138d71de884b46a37934c00bae1b37beefdfd1ef708f047716dab652dc`  
		Last Modified: Mon, 12 May 2025 19:09:44 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250518.0.352066`

**does not exist** (yet?)
