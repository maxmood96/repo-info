<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20251005.0.430597`](#archlinuxbase-202510050430597)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20251005.0.430597`](#archlinuxbase-devel-202510050430597)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20251005.0.430597`](#archlinuxmultilib-devel-202510050430597)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:9a72b5e3c1675683016cb065f513deea7c65836cb5bd22b88c89353098faa40f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:3da61078ff1ed4b4e85416bb9359652ee699d025893a206228a5914c89a9fb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164738114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82680043225b167c73b674f935dfd98729e50bec62d48fff0e4bef0014eb5c2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.version=20250928.0.426921
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.created=2025-09-28T00:07:11+00:00
# Sun, 28 Sep 2025 00:07:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250928.0.426921' /etc/os-release # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
ENV LANG=C.UTF-8
# Sun, 28 Sep 2025 00:07:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f38b8cce2f83b4db2c474585717a2fc37797d6f8e617ba3e29cfc367d9f0af7e`  
		Last Modified: Mon, 29 Sep 2025 17:30:34 GMT  
		Size: 164.7 MB (164729761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e90a4a68db40a24f4b026253e54ef9796ce4b45a04ad7ca427f27c354be8a5`  
		Last Modified: Mon, 29 Sep 2025 17:29:23 GMT  
		Size: 8.4 KB (8353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:2ebf6711bfac6763dc28207679bbac05ba17a528db7d0f74b17e58ab5b1b3ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8228979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c51fa7c6be72241641c887ac4af9f828e2e9091e0a904e8e1e2b1977336f042`

```dockerfile
```

-	Layers:
	-	`sha256:862a0310b99ea050019740c577a0245d00aba587c9667de4b97224fb3fce83ef`  
		Last Modified: Mon, 29 Sep 2025 19:48:18 GMT  
		Size: 8.2 MB (8217007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9784034e7d2ec88ba8358427ec73277584c1a319b5a64b1470f19c7ea825f3`  
		Last Modified: Mon, 29 Sep 2025 19:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251005.0.430597`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:5d95edcb6e10fd865e827e93749ecd425f5056880a5a1d8971f5f2a96c7b5a9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:a76427cd2d3c2153fda2544bb988e9a5a0c6a7c9aeead8f50c437a5cfa3baecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289836820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca91498dc7c82e2e2d19d1a3cc97457d83aebe72b8b9af226adf0e24dca43c9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.version=20250928.0.426921
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.created=2025-09-28T00:07:11+00:00
# Sun, 28 Sep 2025 00:07:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250928.0.426921' /etc/os-release # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
ENV LANG=C.UTF-8
# Sun, 28 Sep 2025 00:07:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:00379b9bac0d799a3b12574884a943b938ea4344c8cc41124041c0afd05ac668`  
		Last Modified: Mon, 29 Sep 2025 19:50:37 GMT  
		Size: 289.8 MB (289827676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e52b0a8b4c1c01761221ef098a893bdd292b95f2a84faade66d02ac0c7302b`  
		Last Modified: Mon, 29 Sep 2025 17:31:05 GMT  
		Size: 9.1 KB (9144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:b449b544ff923113301c2eae816d55b18a395c5ff0e350a830ce079c6fe2c552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90ffebd7845e40d975f69d3b5a946f01bfc3325494150f11e559db34c852a5`

```dockerfile
```

-	Layers:
	-	`sha256:e5644a69415b56b12758dd7e5f1c317dc633928cf9c7cf44a92eac3e57691daa`  
		Last Modified: Mon, 29 Sep 2025 19:48:26 GMT  
		Size: 12.1 MB (12118343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87f634aae0d81b5b9221e128ad4529fdbec5325e74f7ff78036d2e2092a624e`  
		Last Modified: Mon, 29 Sep 2025 19:48:27 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251005.0.430597`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:9a72b5e3c1675683016cb065f513deea7c65836cb5bd22b88c89353098faa40f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:3da61078ff1ed4b4e85416bb9359652ee699d025893a206228a5914c89a9fb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164738114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82680043225b167c73b674f935dfd98729e50bec62d48fff0e4bef0014eb5c2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.version=20250928.0.426921
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.created=2025-09-28T00:07:11+00:00
# Sun, 28 Sep 2025 00:07:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250928.0.426921' /etc/os-release # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
ENV LANG=C.UTF-8
# Sun, 28 Sep 2025 00:07:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f38b8cce2f83b4db2c474585717a2fc37797d6f8e617ba3e29cfc367d9f0af7e`  
		Last Modified: Mon, 29 Sep 2025 17:30:34 GMT  
		Size: 164.7 MB (164729761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e90a4a68db40a24f4b026253e54ef9796ce4b45a04ad7ca427f27c354be8a5`  
		Last Modified: Mon, 29 Sep 2025 17:29:23 GMT  
		Size: 8.4 KB (8353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:2ebf6711bfac6763dc28207679bbac05ba17a528db7d0f74b17e58ab5b1b3ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8228979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c51fa7c6be72241641c887ac4af9f828e2e9091e0a904e8e1e2b1977336f042`

```dockerfile
```

-	Layers:
	-	`sha256:862a0310b99ea050019740c577a0245d00aba587c9667de4b97224fb3fce83ef`  
		Last Modified: Mon, 29 Sep 2025 19:48:18 GMT  
		Size: 8.2 MB (8217007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9784034e7d2ec88ba8358427ec73277584c1a319b5a64b1470f19c7ea825f3`  
		Last Modified: Mon, 29 Sep 2025 19:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:88376c49d29671bdda84f0274d874d2deb7680c921a67df881aa14bee3d1782d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f142967a07452f603ec8c06a0a5702998f8bb6625eaac2677715119caad20c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341155858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8290d444910aa65b516a9a665598535e1852c11a08c62630ed13b19e809e8bdb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.version=20250928.0.426921
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.created=2025-09-28T00:07:11+00:00
# Sun, 28 Sep 2025 00:07:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250928.0.426921' /etc/os-release # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
ENV LANG=C.UTF-8
# Sun, 28 Sep 2025 00:07:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:fa34bc9c8c7971a5a6d6ad411a4d1edfdaad82f213badb3427223ae31a0e7b62`  
		Last Modified: Mon, 29 Sep 2025 20:08:25 GMT  
		Size: 341.1 MB (341145597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce6e0fd4ce0734915d1c0c8164768fe5fc2751618ac97687d91ffdaba8c0c5c`  
		Last Modified: Mon, 29 Sep 2025 17:31:00 GMT  
		Size: 10.3 KB (10261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:e2af8f86891d8c7f2c6a5a752a66a179b7b89a6f7bc346456bbd81ddbe66fb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12398940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170d093347259d57127a005fda160e56160cc0ea051f623111657db7f1564bee`

```dockerfile
```

-	Layers:
	-	`sha256:dbc7e9706418e308a813fae0dba6bc723aef0f937175c5434a97a4967903519f`  
		Last Modified: Mon, 29 Sep 2025 19:48:30 GMT  
		Size: 12.4 MB (12387131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2063d1099c1fa1eecadebec0d0d996f748675dfda68332905d0b89ae8d98d6e0`  
		Last Modified: Mon, 29 Sep 2025 19:48:31 GMT  
		Size: 11.8 KB (11809 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251005.0.430597`

**does not exist** (yet?)
