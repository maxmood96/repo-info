<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250420.0.338771`](#archlinuxbase-202504200338771)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250420.0.338771`](#archlinuxbase-devel-202504200338771)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250420.0.338771`](#archlinuxmultilib-devel-202504200338771)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:ce4dddea70099cc8360478d162e478997420185683ce9de88223c3f316c17c1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:abd76aa5edede07476fabba538e80fdbd54d1326f32ae0bb64efcd3f17c362a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160247595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405a3273f1873dbaf19fb3c110b234dc6c38e7a205f6a6c78c34776545409810`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a1b185628eec31bffbf020fe73a089e4b496c8822b25b0d53c34c05f589a91cc`  
		Last Modified: Mon, 21 Apr 2025 22:34:24 GMT  
		Size: 160.2 MB (160239247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757f0aa62ffe93c4e2a40ba1f2b59a886f3fe59733176db9fa3dca4b9e0276b`  
		Last Modified: Mon, 21 Apr 2025 22:34:20 GMT  
		Size: 8.3 KB (8348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:3efcdf569b00489cc39a9006332f2f4ced799a4a69e32afeed2a427858ab4b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad01ac41f81be3bdd59e7fdcc2d38aaf3a8b6d6583f0162f42abb1351bca5ad`

```dockerfile
```

-	Layers:
	-	`sha256:96a14649829e65702c3656892ebef89369fa00c3e5b5cb2d1aa68db8f7435c86`  
		Last Modified: Mon, 21 Apr 2025 22:34:21 GMT  
		Size: 8.2 MB (8164628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775d65efbd7ee3566bd8680280f412e627b94e92fce89932f923fa9eee06b80c`  
		Last Modified: Mon, 21 Apr 2025 22:34:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250420.0.338771`

```console
$ docker pull archlinux@sha256:ce4dddea70099cc8360478d162e478997420185683ce9de88223c3f316c17c1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250420.0.338771` - linux; amd64

```console
$ docker pull archlinux@sha256:abd76aa5edede07476fabba538e80fdbd54d1326f32ae0bb64efcd3f17c362a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160247595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405a3273f1873dbaf19fb3c110b234dc6c38e7a205f6a6c78c34776545409810`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a1b185628eec31bffbf020fe73a089e4b496c8822b25b0d53c34c05f589a91cc`  
		Last Modified: Mon, 21 Apr 2025 22:34:24 GMT  
		Size: 160.2 MB (160239247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757f0aa62ffe93c4e2a40ba1f2b59a886f3fe59733176db9fa3dca4b9e0276b`  
		Last Modified: Mon, 21 Apr 2025 22:34:20 GMT  
		Size: 8.3 KB (8348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250420.0.338771` - unknown; unknown

```console
$ docker pull archlinux@sha256:3efcdf569b00489cc39a9006332f2f4ced799a4a69e32afeed2a427858ab4b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad01ac41f81be3bdd59e7fdcc2d38aaf3a8b6d6583f0162f42abb1351bca5ad`

```dockerfile
```

-	Layers:
	-	`sha256:96a14649829e65702c3656892ebef89369fa00c3e5b5cb2d1aa68db8f7435c86`  
		Last Modified: Mon, 21 Apr 2025 22:34:21 GMT  
		Size: 8.2 MB (8164628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775d65efbd7ee3566bd8680280f412e627b94e92fce89932f923fa9eee06b80c`  
		Last Modified: Mon, 21 Apr 2025 22:34:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:ef9c9e84828ccedb4cbabfe0a23f636ccd01151c89cad04401afdae4454c2312
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:54c1922f68a1de47fed8b7d6d1db54f555bbd40cbe8e01aa593a2b81be1add6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281760687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781c7b01102859435fa5c5455647eb06070fa91767bbafe89ae28637356aae4e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:83f4100c1b5735024afce8e791c4d3749fe3f86b087ab0210426a12332693945`  
		Last Modified: Mon, 21 Apr 2025 22:34:49 GMT  
		Size: 281.8 MB (281751516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa612d5cc862eac9104b82df9bcbbc7d20689d0086fff0ed0acdddf83b038c4`  
		Last Modified: Mon, 21 Apr 2025 22:34:45 GMT  
		Size: 9.2 KB (9171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:759002d25c04d508019ead0b88bed58d624baf1398b2320942cc0963b265dfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11998045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0a0bd28354a804831d273e7a2205ccd835aac5247523fdd2ba9eb1e4d07358`

```dockerfile
```

-	Layers:
	-	`sha256:2238620d005e2863b7b1ec6f537e1d8b1b21d4356f617e4edf9451e4b2fa1abc`  
		Last Modified: Mon, 21 Apr 2025 22:34:50 GMT  
		Size: 12.0 MB (11986291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c41e7c38413c05affb373aa6b337ca9345e40825a802ec63a2976e48564c3df`  
		Last Modified: Mon, 21 Apr 2025 22:34:45 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250420.0.338771`

```console
$ docker pull archlinux@sha256:ef9c9e84828ccedb4cbabfe0a23f636ccd01151c89cad04401afdae4454c2312
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250420.0.338771` - linux; amd64

```console
$ docker pull archlinux@sha256:54c1922f68a1de47fed8b7d6d1db54f555bbd40cbe8e01aa593a2b81be1add6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281760687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781c7b01102859435fa5c5455647eb06070fa91767bbafe89ae28637356aae4e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:83f4100c1b5735024afce8e791c4d3749fe3f86b087ab0210426a12332693945`  
		Last Modified: Mon, 21 Apr 2025 22:34:49 GMT  
		Size: 281.8 MB (281751516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa612d5cc862eac9104b82df9bcbbc7d20689d0086fff0ed0acdddf83b038c4`  
		Last Modified: Mon, 21 Apr 2025 22:34:45 GMT  
		Size: 9.2 KB (9171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250420.0.338771` - unknown; unknown

```console
$ docker pull archlinux@sha256:759002d25c04d508019ead0b88bed58d624baf1398b2320942cc0963b265dfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11998045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0a0bd28354a804831d273e7a2205ccd835aac5247523fdd2ba9eb1e4d07358`

```dockerfile
```

-	Layers:
	-	`sha256:2238620d005e2863b7b1ec6f537e1d8b1b21d4356f617e4edf9451e4b2fa1abc`  
		Last Modified: Mon, 21 Apr 2025 22:34:50 GMT  
		Size: 12.0 MB (11986291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c41e7c38413c05affb373aa6b337ca9345e40825a802ec63a2976e48564c3df`  
		Last Modified: Mon, 21 Apr 2025 22:34:45 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:ce4dddea70099cc8360478d162e478997420185683ce9de88223c3f316c17c1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:abd76aa5edede07476fabba538e80fdbd54d1326f32ae0bb64efcd3f17c362a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160247595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405a3273f1873dbaf19fb3c110b234dc6c38e7a205f6a6c78c34776545409810`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a1b185628eec31bffbf020fe73a089e4b496c8822b25b0d53c34c05f589a91cc`  
		Last Modified: Mon, 21 Apr 2025 22:34:24 GMT  
		Size: 160.2 MB (160239247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757f0aa62ffe93c4e2a40ba1f2b59a886f3fe59733176db9fa3dca4b9e0276b`  
		Last Modified: Mon, 21 Apr 2025 22:34:20 GMT  
		Size: 8.3 KB (8348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:3efcdf569b00489cc39a9006332f2f4ced799a4a69e32afeed2a427858ab4b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad01ac41f81be3bdd59e7fdcc2d38aaf3a8b6d6583f0162f42abb1351bca5ad`

```dockerfile
```

-	Layers:
	-	`sha256:96a14649829e65702c3656892ebef89369fa00c3e5b5cb2d1aa68db8f7435c86`  
		Last Modified: Mon, 21 Apr 2025 22:34:21 GMT  
		Size: 8.2 MB (8164628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775d65efbd7ee3566bd8680280f412e627b94e92fce89932f923fa9eee06b80c`  
		Last Modified: Mon, 21 Apr 2025 22:34:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:a9454267500cb19e43ce9d8f276021f60ac16f90b90a5b94cdae8c0619e58266
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:a31b1a042ca97f5980e5f3042b8107ab1c8089d7754fae7903652c38a42fd5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331756959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7498f9f422b380616dae9cf2b35fdd81d50035db475d0195da20034dbfb84781`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:974b446697e9df1a9de12f2eee3522356a152f031b88796f709ddff7138a73cb`  
		Last Modified: Mon, 21 Apr 2025 22:35:20 GMT  
		Size: 331.7 MB (331746663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42aad208d10e2a974370e88bbe7c59ef5ea182002c108842f8a82a37b803b`  
		Last Modified: Mon, 21 Apr 2025 22:35:10 GMT  
		Size: 10.3 KB (10296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:816bec377024b31c9d0e9301336b59bac8de6afedfbbe074df59b2c20b7d2045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12266637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c0e0f29d3dd8863ce24bf061124be99d59ab2f3ee3a65c083372f481edc854`

```dockerfile
```

-	Layers:
	-	`sha256:eb89539594f1987717d8d678eee84c24982c8f4f95486eaf1ddee199b2373cfb`  
		Last Modified: Mon, 21 Apr 2025 22:35:11 GMT  
		Size: 12.3 MB (12254826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a0ccd60cf8cc9a43c4787fa23fb1bd98836285be840075c8d826a4ae56fc01`  
		Last Modified: Mon, 21 Apr 2025 22:35:10 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250420.0.338771`

```console
$ docker pull archlinux@sha256:a9454267500cb19e43ce9d8f276021f60ac16f90b90a5b94cdae8c0619e58266
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250420.0.338771` - linux; amd64

```console
$ docker pull archlinux@sha256:a31b1a042ca97f5980e5f3042b8107ab1c8089d7754fae7903652c38a42fd5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331756959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7498f9f422b380616dae9cf2b35fdd81d50035db475d0195da20034dbfb84781`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:974b446697e9df1a9de12f2eee3522356a152f031b88796f709ddff7138a73cb`  
		Last Modified: Mon, 21 Apr 2025 22:35:20 GMT  
		Size: 331.7 MB (331746663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42aad208d10e2a974370e88bbe7c59ef5ea182002c108842f8a82a37b803b`  
		Last Modified: Mon, 21 Apr 2025 22:35:10 GMT  
		Size: 10.3 KB (10296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250420.0.338771` - unknown; unknown

```console
$ docker pull archlinux@sha256:816bec377024b31c9d0e9301336b59bac8de6afedfbbe074df59b2c20b7d2045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12266637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c0e0f29d3dd8863ce24bf061124be99d59ab2f3ee3a65c083372f481edc854`

```dockerfile
```

-	Layers:
	-	`sha256:eb89539594f1987717d8d678eee84c24982c8f4f95486eaf1ddee199b2373cfb`  
		Last Modified: Mon, 21 Apr 2025 22:35:11 GMT  
		Size: 12.3 MB (12254826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a0ccd60cf8cc9a43c4787fa23fb1bd98836285be840075c8d826a4ae56fc01`  
		Last Modified: Mon, 21 Apr 2025 22:35:10 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
