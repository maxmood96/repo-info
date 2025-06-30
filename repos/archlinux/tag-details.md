<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250629.0.373469`](#archlinuxbase-202506290373469)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250629.0.373469`](#archlinuxbase-devel-202506290373469)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250629.0.373469`](#archlinuxmultilib-devel-202506290373469)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:a921b6864609280975d8269df323c2f4f478cdc9d0f5479e70c3fb5e710d1b11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:e7eda50a054df84145bd4b9ef1231d0efae47b4fab526eb8df171cacc5766565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163065097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683780d7bb0bd9086019f3ff532ef3a75b3f4a8143b4bbb0ac640ec4d1f2de90`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250622.0.370030
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-06-22T00:07:28+00:00
# Sun, 22 Jun 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250622.0.370030' /etc/os-release # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Jun 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9d37d6e63884857da7d1b14c93a397e958c93ba2ed8a5d80ca61722c48c9fbdf`  
		Last Modified: Mon, 23 Jun 2025 18:35:13 GMT  
		Size: 163.1 MB (163056750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd720a8b0d34871aa7ad437d570670de7eb94c7e7a2a43694ae3f27b273287b3`  
		Last Modified: Mon, 23 Jun 2025 16:52:06 GMT  
		Size: 8.3 KB (8347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:de1c487256a3b6c00c8490bc8c3d947ae88146b591a70b6f5aeb70fd7cc91029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b21c0d991dd08e679964c41de77dfb2c8c8a405f1dd24b0c9c28225200df64`

```dockerfile
```

-	Layers:
	-	`sha256:ede6771150cd0113fe48afbf2e5fc38584daed1537b80feb81cdb9c4abf93275`  
		Last Modified: Mon, 23 Jun 2025 19:48:16 GMT  
		Size: 8.1 MB (8148140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126ea1eb77f86ad9cdcc639ad746568837ab37c787aa9ce17a64ebb05697fe9a`  
		Last Modified: Mon, 23 Jun 2025 19:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250629.0.373469`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:bb4464b24c12e523070bc5e70412e318843d1ff37494f11ddd7f12a623547636
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c6f1b4688d4649b9ea1bdb216df51c814752ebaa9952e0ff1d41f6d8a3f4e0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287731717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7216526a2328c46175e1f8cc7af7254ce3a81a06c1d1992277bc6dd767faef`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250622.0.370030
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-06-22T00:07:28+00:00
# Sun, 22 Jun 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250622.0.370030' /etc/os-release # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Jun 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1ba9e09b0af0cd7f0a5cd4c784ef2ba0fa25425deb576571a76d3e74acfa7dbe`  
		Last Modified: Mon, 23 Jun 2025 19:50:58 GMT  
		Size: 287.7 MB (287722555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e26c361e60b00e0972f1623311805b4ae0275b554d6a17e4afb27a9b8c2d3b7`  
		Last Modified: Mon, 23 Jun 2025 16:52:19 GMT  
		Size: 9.2 KB (9162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:65c715f6c7997d259484f3898fad301641da83de0e003c0a431cc196b0c78f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12021360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becde3ab19cf14e988ed6abbca570cdf76bd9af99dee9713a49d2190ebb2df41`

```dockerfile
```

-	Layers:
	-	`sha256:2ec34fc42052f3b04fedf19260ada55424eb0b0f7f559aa42a405705dc5ea3f8`  
		Last Modified: Mon, 23 Jun 2025 19:48:21 GMT  
		Size: 12.0 MB (12009607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1124fc950523b8cfb893ca5620330fc93df9ce76ac5a02704794d746dd459be`  
		Last Modified: Mon, 23 Jun 2025 19:48:22 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250629.0.373469`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a921b6864609280975d8269df323c2f4f478cdc9d0f5479e70c3fb5e710d1b11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e7eda50a054df84145bd4b9ef1231d0efae47b4fab526eb8df171cacc5766565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163065097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683780d7bb0bd9086019f3ff532ef3a75b3f4a8143b4bbb0ac640ec4d1f2de90`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250622.0.370030
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-06-22T00:07:28+00:00
# Sun, 22 Jun 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250622.0.370030' /etc/os-release # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Jun 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9d37d6e63884857da7d1b14c93a397e958c93ba2ed8a5d80ca61722c48c9fbdf`  
		Last Modified: Mon, 23 Jun 2025 18:35:13 GMT  
		Size: 163.1 MB (163056750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd720a8b0d34871aa7ad437d570670de7eb94c7e7a2a43694ae3f27b273287b3`  
		Last Modified: Mon, 23 Jun 2025 16:52:06 GMT  
		Size: 8.3 KB (8347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:de1c487256a3b6c00c8490bc8c3d947ae88146b591a70b6f5aeb70fd7cc91029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b21c0d991dd08e679964c41de77dfb2c8c8a405f1dd24b0c9c28225200df64`

```dockerfile
```

-	Layers:
	-	`sha256:ede6771150cd0113fe48afbf2e5fc38584daed1537b80feb81cdb9c4abf93275`  
		Last Modified: Mon, 23 Jun 2025 19:48:16 GMT  
		Size: 8.1 MB (8148140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126ea1eb77f86ad9cdcc639ad746568837ab37c787aa9ce17a64ebb05697fe9a`  
		Last Modified: Mon, 23 Jun 2025 19:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:528e9633b78ea2c2044b58b61199b00f7c05484ceaaf38ce6365a6171bf5a12f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:80530de0623809411a822facba5b22bd4eac34ec03c732a8050d425ba41a7491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338895365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e65f705ba451809814adbd5372ab385234a15dc1b21f0bef0a6efb036d1c2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250622.0.370030
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-06-22T00:07:28+00:00
# Sun, 22 Jun 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250622.0.370030' /etc/os-release # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Jun 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c0d08995da1c28452b383d3dd1b586f235d9e3d8ec35ee5ff1507e5a330cfdad`  
		Last Modified: Mon, 23 Jun 2025 19:52:32 GMT  
		Size: 338.9 MB (338885115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10dd6e569b7f68cf63e3e269781f893165a9cf721b6a4a8331edfc5c5666e81`  
		Last Modified: Mon, 23 Jun 2025 16:53:06 GMT  
		Size: 10.2 KB (10250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:4b78d5ff04c410cf8d98378c130eccf537b2b637bb6f4098f718549019264fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12290307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d6d9432cb34441f7414593c39402badc2e1f4511e0a2925f347fcbb3af9562`

```dockerfile
```

-	Layers:
	-	`sha256:72a9faa471318afefcfc7057379d2082101f9a0316b542cd757ff4e8334b3e09`  
		Last Modified: Mon, 23 Jun 2025 19:48:25 GMT  
		Size: 12.3 MB (12278496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25d77b6846e61c76fdfaec27f583f74f3e43254962023bb9423b16d9abf96d`  
		Last Modified: Mon, 23 Jun 2025 19:48:26 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250629.0.373469`

**does not exist** (yet?)
