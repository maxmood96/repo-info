<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260531.0.538839`](#archlinuxbase-202605310538839)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260531.0.538839`](#archlinuxbase-devel-202605310538839)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260531.0.538839`](#archlinuxmultilib-devel-202605310538839)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:a9a1e6db522cf5f8018c920d035e2bfbf8e39c485ee737ce0388990898f2f042
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0c3d22e3d4dad2296ad03dcaddfb86846ede60cc4ad38024dc893b3a0057d3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131939728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f760002b3b4da50eef8689003a869a7bbfc1c60da0e1c7bb9bb55783a1b34f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:30:27 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:30:30 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:30:30 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:30:30 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d4254956de0f617437e75abca155a64fd85babfcbe5c7fcec105ad776d3fa728`  
		Last Modified: Mon, 01 Jun 2026 21:30:57 GMT  
		Size: 131.9 MB (131931052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67503bd63c157a0bb8e0f7e938186c40487e3e1c6cc64125f76a4ef00bac2cf0`  
		Last Modified: Mon, 01 Jun 2026 21:30:55 GMT  
		Size: 8.7 KB (8676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:5787bcda05b3556730c70c116ce710522687a21b325c7dc5beeca5e49e0d036b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3c4f103d3539e8e5c2ec40e941c00e8e8abb6793bbdbcdd3deb24f5381e68c`

```dockerfile
```

-	Layers:
	-	`sha256:0aa426b73e32328de6e058b789c9af7e5c56a2848c50a20c77e2fc05ead23162`  
		Last Modified: Mon, 01 Jun 2026 21:30:54 GMT  
		Size: 8.2 MB (8181157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1b13ac0e0690ce443e24656b5d7f63acd74453e1351b7cd6aae989a48c562c`  
		Last Modified: Mon, 01 Jun 2026 21:30:54 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260531.0.538839`

```console
$ docker pull archlinux@sha256:a9a1e6db522cf5f8018c920d035e2bfbf8e39c485ee737ce0388990898f2f042
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260531.0.538839` - linux; amd64

```console
$ docker pull archlinux@sha256:0c3d22e3d4dad2296ad03dcaddfb86846ede60cc4ad38024dc893b3a0057d3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131939728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f760002b3b4da50eef8689003a869a7bbfc1c60da0e1c7bb9bb55783a1b34f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:30:27 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:30:30 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:30:30 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:30:30 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d4254956de0f617437e75abca155a64fd85babfcbe5c7fcec105ad776d3fa728`  
		Last Modified: Mon, 01 Jun 2026 21:30:57 GMT  
		Size: 131.9 MB (131931052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67503bd63c157a0bb8e0f7e938186c40487e3e1c6cc64125f76a4ef00bac2cf0`  
		Last Modified: Mon, 01 Jun 2026 21:30:55 GMT  
		Size: 8.7 KB (8676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260531.0.538839` - unknown; unknown

```console
$ docker pull archlinux@sha256:5787bcda05b3556730c70c116ce710522687a21b325c7dc5beeca5e49e0d036b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3c4f103d3539e8e5c2ec40e941c00e8e8abb6793bbdbcdd3deb24f5381e68c`

```dockerfile
```

-	Layers:
	-	`sha256:0aa426b73e32328de6e058b789c9af7e5c56a2848c50a20c77e2fc05ead23162`  
		Last Modified: Mon, 01 Jun 2026 21:30:54 GMT  
		Size: 8.2 MB (8181157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1b13ac0e0690ce443e24656b5d7f63acd74453e1351b7cd6aae989a48c562c`  
		Last Modified: Mon, 01 Jun 2026 21:30:54 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c84ad63503efc5d386e30a5f44945fa8eee10fcb21b3d5fceda260783de394ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b020e4b83a278d78028c89186b7f937a92e57a59d800587b713af7f9bfc0d45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304004094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a65e6928d31336af0d1c66eae039c6bb18d2ab7872b527495aa306a5121de`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:31:03 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:31:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:31:16 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:31:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9f04e3f1a44c3fcba4c558a3b057780df3a688b4965c0d7268b6118b903351f`  
		Last Modified: Mon, 01 Jun 2026 21:32:08 GMT  
		Size: 304.0 MB (303992683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5afeb8ece19bbc8a93dc14d6de8929c291eac60f32b49067e9806c8abf253c`  
		Last Modified: Mon, 01 Jun 2026 21:32:00 GMT  
		Size: 11.4 KB (11411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:15ea0abd8e9b686b416de361fc609d3ad69a6501dc5d103bccb61b311dee2df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14396300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7d33c344487675eef6e28c739bb29f0dd4ee66301a800c6be9ae9e90e93517`

```dockerfile
```

-	Layers:
	-	`sha256:9074331b3600b9122731310f1090ebdfbef5b80ba81c3c69d455561c7325a10d`  
		Last Modified: Mon, 01 Jun 2026 21:32:01 GMT  
		Size: 14.4 MB (14384588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ad73ec17231b9ea1f9aa8ab786c5b63aa92b632e23a4680da5f40cedbbf4487`  
		Last Modified: Mon, 01 Jun 2026 21:32:00 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260531.0.538839`

```console
$ docker pull archlinux@sha256:c84ad63503efc5d386e30a5f44945fa8eee10fcb21b3d5fceda260783de394ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260531.0.538839` - linux; amd64

```console
$ docker pull archlinux@sha256:b020e4b83a278d78028c89186b7f937a92e57a59d800587b713af7f9bfc0d45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304004094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a65e6928d31336af0d1c66eae039c6bb18d2ab7872b527495aa306a5121de`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:31:03 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:31:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:31:16 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:31:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9f04e3f1a44c3fcba4c558a3b057780df3a688b4965c0d7268b6118b903351f`  
		Last Modified: Mon, 01 Jun 2026 21:32:08 GMT  
		Size: 304.0 MB (303992683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5afeb8ece19bbc8a93dc14d6de8929c291eac60f32b49067e9806c8abf253c`  
		Last Modified: Mon, 01 Jun 2026 21:32:00 GMT  
		Size: 11.4 KB (11411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260531.0.538839` - unknown; unknown

```console
$ docker pull archlinux@sha256:15ea0abd8e9b686b416de361fc609d3ad69a6501dc5d103bccb61b311dee2df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14396300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7d33c344487675eef6e28c739bb29f0dd4ee66301a800c6be9ae9e90e93517`

```dockerfile
```

-	Layers:
	-	`sha256:9074331b3600b9122731310f1090ebdfbef5b80ba81c3c69d455561c7325a10d`  
		Last Modified: Mon, 01 Jun 2026 21:32:01 GMT  
		Size: 14.4 MB (14384588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ad73ec17231b9ea1f9aa8ab786c5b63aa92b632e23a4680da5f40cedbbf4487`  
		Last Modified: Mon, 01 Jun 2026 21:32:00 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a9a1e6db522cf5f8018c920d035e2bfbf8e39c485ee737ce0388990898f2f042
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0c3d22e3d4dad2296ad03dcaddfb86846ede60cc4ad38024dc893b3a0057d3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131939728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f760002b3b4da50eef8689003a869a7bbfc1c60da0e1c7bb9bb55783a1b34f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:30:27 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:30:27 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:30:30 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:30:30 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:30:30 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d4254956de0f617437e75abca155a64fd85babfcbe5c7fcec105ad776d3fa728`  
		Last Modified: Mon, 01 Jun 2026 21:30:57 GMT  
		Size: 131.9 MB (131931052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67503bd63c157a0bb8e0f7e938186c40487e3e1c6cc64125f76a4ef00bac2cf0`  
		Last Modified: Mon, 01 Jun 2026 21:30:55 GMT  
		Size: 8.7 KB (8676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:5787bcda05b3556730c70c116ce710522687a21b325c7dc5beeca5e49e0d036b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3c4f103d3539e8e5c2ec40e941c00e8e8abb6793bbdbcdd3deb24f5381e68c`

```dockerfile
```

-	Layers:
	-	`sha256:0aa426b73e32328de6e058b789c9af7e5c56a2848c50a20c77e2fc05ead23162`  
		Last Modified: Mon, 01 Jun 2026 21:30:54 GMT  
		Size: 8.2 MB (8181157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1b13ac0e0690ce443e24656b5d7f63acd74453e1351b7cd6aae989a48c562c`  
		Last Modified: Mon, 01 Jun 2026 21:30:54 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:ac45720cd4e51daff8f164699bc83662386e5247906b78e85098de210de6c839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5acd74e1ec80246e5428e9fb833109555b9981629ec8fd30ea39863528b1c174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326397104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1700b1308251bd3b3753f8e2397827d22b5ba0220c2cd0fb076eab011efbd0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:31:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:31:13 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:31:13 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:31:13 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:183d3e1c43c83600bb5f00d3fabd0bca7e80c7e5db7c5c49f6ec47c8d31a1f4c`  
		Last Modified: Mon, 01 Jun 2026 21:32:19 GMT  
		Size: 326.4 MB (326384561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e75021c7a376af5d4ed3aca9430442b41fcc90e6e5a08975482a8de7cc2a47`  
		Last Modified: Mon, 01 Jun 2026 21:32:06 GMT  
		Size: 12.5 KB (12543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:44afef308412338fa806f5bc52fe5b5de07c28bdb63c1898c77937230b6b591a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14667097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2079080fdf437c5239e148a040778f51f10fb063a6552141a884653c4589a5`

```dockerfile
```

-	Layers:
	-	`sha256:253edf92189c79a07ccb7f655585add73cb8aa0577e836a5d6338d88a7bfa25f`  
		Last Modified: Mon, 01 Jun 2026 21:32:07 GMT  
		Size: 14.7 MB (14655329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f93ca7905912e7fb1d25286b614911069966a4eaf3fa3c0cb0a07133130890`  
		Last Modified: Mon, 01 Jun 2026 21:32:06 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260531.0.538839`

```console
$ docker pull archlinux@sha256:ac45720cd4e51daff8f164699bc83662386e5247906b78e85098de210de6c839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260531.0.538839` - linux; amd64

```console
$ docker pull archlinux@sha256:5acd74e1ec80246e5428e9fb833109555b9981629ec8fd30ea39863528b1c174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326397104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1700b1308251bd3b3753f8e2397827d22b5ba0220c2cd0fb076eab011efbd0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:31:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:31:13 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:31:13 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:31:13 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:183d3e1c43c83600bb5f00d3fabd0bca7e80c7e5db7c5c49f6ec47c8d31a1f4c`  
		Last Modified: Mon, 01 Jun 2026 21:32:19 GMT  
		Size: 326.4 MB (326384561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e75021c7a376af5d4ed3aca9430442b41fcc90e6e5a08975482a8de7cc2a47`  
		Last Modified: Mon, 01 Jun 2026 21:32:06 GMT  
		Size: 12.5 KB (12543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260531.0.538839` - unknown; unknown

```console
$ docker pull archlinux@sha256:44afef308412338fa806f5bc52fe5b5de07c28bdb63c1898c77937230b6b591a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14667097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2079080fdf437c5239e148a040778f51f10fb063a6552141a884653c4589a5`

```dockerfile
```

-	Layers:
	-	`sha256:253edf92189c79a07ccb7f655585add73cb8aa0577e836a5d6338d88a7bfa25f`  
		Last Modified: Mon, 01 Jun 2026 21:32:07 GMT  
		Size: 14.7 MB (14655329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f93ca7905912e7fb1d25286b614911069966a4eaf3fa3c0cb0a07133130890`  
		Last Modified: Mon, 01 Jun 2026 21:32:06 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
