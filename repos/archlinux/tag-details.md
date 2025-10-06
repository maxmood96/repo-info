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
$ docker pull archlinux@sha256:ca6af8049bd9dee3eb2bc3d620642ca1bc81b00f10aa08b12ee28ac56063be49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a8904aee9b0599e9b0497d49195dfb8beb94b3c01a7bb56ec18168143f810655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165272328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a450996096cb455fccd0e5fd50f9c5390ee1c1f4e7f390b9a90ec74281549d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f76ba238a84a63b71e658023be058526928f3de0dcb19747c2a10d5a20567f04`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 165.3 MB (165263996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afbbb9519488fa765e35f101d286e1fb1e617085d1373cb282b33fa59079619`  
		Last Modified: Mon, 06 Oct 2025 18:07:47 GMT  
		Size: 8.3 KB (8332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:f072fbe3c36425cecfa820b581547be2571cb1f536a8747e276a4c3644803838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8230220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37929c702aa964aa6174ed85bf6006a935a4cac62fd9923e03b7a333df204396`

```dockerfile
```

-	Layers:
	-	`sha256:ad85159e1193664cb877e2ffd5521402aca2b5a192629369fe964608538ef30a`  
		Last Modified: Mon, 06 Oct 2025 19:48:19 GMT  
		Size: 8.2 MB (8218248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae50ed92a734e6ec6d3600faf7f79848c408da8b56946cdbb50a59677c2a5182`  
		Last Modified: Mon, 06 Oct 2025 19:48:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251005.0.430597`

```console
$ docker pull archlinux@sha256:ca6af8049bd9dee3eb2bc3d620642ca1bc81b00f10aa08b12ee28ac56063be49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20251005.0.430597` - linux; amd64

```console
$ docker pull archlinux@sha256:a8904aee9b0599e9b0497d49195dfb8beb94b3c01a7bb56ec18168143f810655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165272328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a450996096cb455fccd0e5fd50f9c5390ee1c1f4e7f390b9a90ec74281549d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f76ba238a84a63b71e658023be058526928f3de0dcb19747c2a10d5a20567f04`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 165.3 MB (165263996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afbbb9519488fa765e35f101d286e1fb1e617085d1373cb282b33fa59079619`  
		Last Modified: Mon, 06 Oct 2025 18:07:47 GMT  
		Size: 8.3 KB (8332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20251005.0.430597` - unknown; unknown

```console
$ docker pull archlinux@sha256:f072fbe3c36425cecfa820b581547be2571cb1f536a8747e276a4c3644803838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8230220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37929c702aa964aa6174ed85bf6006a935a4cac62fd9923e03b7a333df204396`

```dockerfile
```

-	Layers:
	-	`sha256:ad85159e1193664cb877e2ffd5521402aca2b5a192629369fe964608538ef30a`  
		Last Modified: Mon, 06 Oct 2025 19:48:19 GMT  
		Size: 8.2 MB (8218248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae50ed92a734e6ec6d3600faf7f79848c408da8b56946cdbb50a59677c2a5182`  
		Last Modified: Mon, 06 Oct 2025 19:48:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b3809917ab5a7840d42237f5f92d92660cd036bd75ae343e7825e6a24401f166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:2f0f0994fcffdfa3d183aeb3ba6190bb67d4d180987ff566673173ee4f926378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290344795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5444ec66413f3126eab60368d32a466728c59ca1297eaea3ded36afc9608a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:31bd40284997e57aafb1578009aa7ac3eb161d57ef18a8620487b68765949955`  
		Last Modified: Mon, 06 Oct 2025 19:48:54 GMT  
		Size: 290.3 MB (290335625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0b90acc81c520a9d4565ebfecb4782cf769176ff2c131f34140f98407cca7`  
		Last Modified: Mon, 06 Oct 2025 17:56:13 GMT  
		Size: 9.2 KB (9170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:fdc3321b047599f5e4255ac1a5f549c462dd47466e1cf20b9a5a4a4bed8774ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12131338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbc7d5218e69dba0997074cae341e477f2cb05a570d0b3f8c3dea98accdc63d`

```dockerfile
```

-	Layers:
	-	`sha256:7763996dbe32382a63a8c5b101ac4fa133c1de8a74367c81428224b0c7838142`  
		Last Modified: Mon, 06 Oct 2025 19:48:31 GMT  
		Size: 12.1 MB (12119584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e7ccd02f79cae45ada89ad2554c01a9d5f597a7c8fe03da86013e13ec4c689`  
		Last Modified: Mon, 06 Oct 2025 19:48:32 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251005.0.430597`

```console
$ docker pull archlinux@sha256:b3809917ab5a7840d42237f5f92d92660cd036bd75ae343e7825e6a24401f166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251005.0.430597` - linux; amd64

```console
$ docker pull archlinux@sha256:2f0f0994fcffdfa3d183aeb3ba6190bb67d4d180987ff566673173ee4f926378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290344795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5444ec66413f3126eab60368d32a466728c59ca1297eaea3ded36afc9608a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:31bd40284997e57aafb1578009aa7ac3eb161d57ef18a8620487b68765949955`  
		Last Modified: Mon, 06 Oct 2025 19:48:54 GMT  
		Size: 290.3 MB (290335625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0b90acc81c520a9d4565ebfecb4782cf769176ff2c131f34140f98407cca7`  
		Last Modified: Mon, 06 Oct 2025 17:56:13 GMT  
		Size: 9.2 KB (9170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251005.0.430597` - unknown; unknown

```console
$ docker pull archlinux@sha256:fdc3321b047599f5e4255ac1a5f549c462dd47466e1cf20b9a5a4a4bed8774ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12131338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbc7d5218e69dba0997074cae341e477f2cb05a570d0b3f8c3dea98accdc63d`

```dockerfile
```

-	Layers:
	-	`sha256:7763996dbe32382a63a8c5b101ac4fa133c1de8a74367c81428224b0c7838142`  
		Last Modified: Mon, 06 Oct 2025 19:48:31 GMT  
		Size: 12.1 MB (12119584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e7ccd02f79cae45ada89ad2554c01a9d5f597a7c8fe03da86013e13ec4c689`  
		Last Modified: Mon, 06 Oct 2025 19:48:32 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:ca6af8049bd9dee3eb2bc3d620642ca1bc81b00f10aa08b12ee28ac56063be49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:a8904aee9b0599e9b0497d49195dfb8beb94b3c01a7bb56ec18168143f810655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165272328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a450996096cb455fccd0e5fd50f9c5390ee1c1f4e7f390b9a90ec74281549d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f76ba238a84a63b71e658023be058526928f3de0dcb19747c2a10d5a20567f04`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 165.3 MB (165263996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afbbb9519488fa765e35f101d286e1fb1e617085d1373cb282b33fa59079619`  
		Last Modified: Mon, 06 Oct 2025 18:07:47 GMT  
		Size: 8.3 KB (8332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:f072fbe3c36425cecfa820b581547be2571cb1f536a8747e276a4c3644803838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8230220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37929c702aa964aa6174ed85bf6006a935a4cac62fd9923e03b7a333df204396`

```dockerfile
```

-	Layers:
	-	`sha256:ad85159e1193664cb877e2ffd5521402aca2b5a192629369fe964608538ef30a`  
		Last Modified: Mon, 06 Oct 2025 19:48:19 GMT  
		Size: 8.2 MB (8218248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae50ed92a734e6ec6d3600faf7f79848c408da8b56946cdbb50a59677c2a5182`  
		Last Modified: Mon, 06 Oct 2025 19:48:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9c2a97563205f30cee1b89eadd37e395b95119a2beb5c3d47ba6eb5c66c566c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:849a203ca9d073b4a0e6319f894058651f5ff820782d98551fc32fbc01609a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341657929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7198f253c58fdd64bb79f20545d75bfe684c7c6ae6d32a9772d221faf7b77499`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:57d32341d0b304edbdd20efcf9481afeb1fb71b457948c77d909ebc150363d3e`  
		Last Modified: Mon, 06 Oct 2025 19:51:26 GMT  
		Size: 341.6 MB (341647654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef2d5695280fef0de17375d8fc55aad6a24e3a57f486684d7c1ec271748ec15`  
		Last Modified: Mon, 06 Oct 2025 18:55:35 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c1d30bcfa1c166f36cecda5e159a8899d174af36aaeba4b0e7f4dad1420c6bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12400183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640f98c73b416a4cdd411101b281c688ce08ccbc1f79b8728accbf166fc122c`

```dockerfile
```

-	Layers:
	-	`sha256:1fc784a31e518e40643ca31df64bade42c39955b1ebfa24ec82662f6c1aeb1ff`  
		Last Modified: Mon, 06 Oct 2025 19:48:33 GMT  
		Size: 12.4 MB (12388372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22eacafbbc8af6591d002ca0b066e314ef827d493d5283e795026e4a1004230`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251005.0.430597`

```console
$ docker pull archlinux@sha256:9c2a97563205f30cee1b89eadd37e395b95119a2beb5c3d47ba6eb5c66c566c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251005.0.430597` - linux; amd64

```console
$ docker pull archlinux@sha256:849a203ca9d073b4a0e6319f894058651f5ff820782d98551fc32fbc01609a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341657929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7198f253c58fdd64bb79f20545d75bfe684c7c6ae6d32a9772d221faf7b77499`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:57d32341d0b304edbdd20efcf9481afeb1fb71b457948c77d909ebc150363d3e`  
		Last Modified: Mon, 06 Oct 2025 19:51:26 GMT  
		Size: 341.6 MB (341647654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef2d5695280fef0de17375d8fc55aad6a24e3a57f486684d7c1ec271748ec15`  
		Last Modified: Mon, 06 Oct 2025 18:55:35 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251005.0.430597` - unknown; unknown

```console
$ docker pull archlinux@sha256:c1d30bcfa1c166f36cecda5e159a8899d174af36aaeba4b0e7f4dad1420c6bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12400183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640f98c73b416a4cdd411101b281c688ce08ccbc1f79b8728accbf166fc122c`

```dockerfile
```

-	Layers:
	-	`sha256:1fc784a31e518e40643ca31df64bade42c39955b1ebfa24ec82662f6c1aeb1ff`  
		Last Modified: Mon, 06 Oct 2025 19:48:33 GMT  
		Size: 12.4 MB (12388372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22eacafbbc8af6591d002ca0b066e314ef827d493d5283e795026e4a1004230`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
