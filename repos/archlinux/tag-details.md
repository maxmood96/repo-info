<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250615.0.365905`](#archlinuxbase-202506150365905)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250615.0.365905`](#archlinuxbase-devel-202506150365905)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250615.0.365905`](#archlinuxmultilib-devel-202506150365905)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:1a39198fcde68348c49a3fd78a54ced553af8168252c6222451f3fe943a4f7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:39f8172042016257f636967d77cfc11734cd9d5e372ad9489320706529ad96ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163047436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f454de10f672ef4f62e2ec1773bbdabb11673efa1b8c6ae2cd1efcf2e9447886`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2459e742a75074b2c8411917dea3d0e8805c859a8ffeb97721ec791c8a915fc2`  
		Last Modified: Mon, 16 Jun 2025 18:44:35 GMT  
		Size: 163.0 MB (163039096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd36e9a0c83950ba1c7fa16e989e8c15d85f200653423c255f1d591128e9c48`  
		Last Modified: Mon, 16 Jun 2025 17:09:40 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:7454d301fe6ce0b57517c165a887683b4a40c3a0d2313485df894f090790aa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb1b4194181934f13d3b3a417c67a4779cc5cc2b24c288f1a990af94e2ea662`

```dockerfile
```

-	Layers:
	-	`sha256:8c4c0334a3a3c5dc9750da23a7aac8b5a9a55b7ca5288d08fee25a9ef8fb34a8`  
		Last Modified: Mon, 16 Jun 2025 19:48:18 GMT  
		Size: 8.1 MB (8148072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038c36bba30c43529cbb600942ffd32f99d7f07b674a33145b056407f662548f`  
		Last Modified: Mon, 16 Jun 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250615.0.365905`

```console
$ docker pull archlinux@sha256:1a39198fcde68348c49a3fd78a54ced553af8168252c6222451f3fe943a4f7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250615.0.365905` - linux; amd64

```console
$ docker pull archlinux@sha256:39f8172042016257f636967d77cfc11734cd9d5e372ad9489320706529ad96ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163047436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f454de10f672ef4f62e2ec1773bbdabb11673efa1b8c6ae2cd1efcf2e9447886`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2459e742a75074b2c8411917dea3d0e8805c859a8ffeb97721ec791c8a915fc2`  
		Last Modified: Mon, 16 Jun 2025 18:44:35 GMT  
		Size: 163.0 MB (163039096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd36e9a0c83950ba1c7fa16e989e8c15d85f200653423c255f1d591128e9c48`  
		Last Modified: Mon, 16 Jun 2025 17:09:40 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250615.0.365905` - unknown; unknown

```console
$ docker pull archlinux@sha256:7454d301fe6ce0b57517c165a887683b4a40c3a0d2313485df894f090790aa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb1b4194181934f13d3b3a417c67a4779cc5cc2b24c288f1a990af94e2ea662`

```dockerfile
```

-	Layers:
	-	`sha256:8c4c0334a3a3c5dc9750da23a7aac8b5a9a55b7ca5288d08fee25a9ef8fb34a8`  
		Last Modified: Mon, 16 Jun 2025 19:48:18 GMT  
		Size: 8.1 MB (8148072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038c36bba30c43529cbb600942ffd32f99d7f07b674a33145b056407f662548f`  
		Last Modified: Mon, 16 Jun 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:3f808d41e09261904a04709fc210a154ee56f6a9c369a15a70c2dfac5adab498
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:00ddc0f2cdfa19e54f164037d768901f8fb81a1aa6a5b2907d259a6729be2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287711663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb635301b5860ac61bbf7aa404a7a2e5faa5f9b4aa967be5853c38db48f92f8e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f4798adc81b48051de112e7ae73136962449d8ea7e2ca5cdbcffd11241616ca6`  
		Last Modified: Mon, 16 Jun 2025 19:48:43 GMT  
		Size: 287.7 MB (287702494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a65be26e0401c45bc2b22a0dd51d271a1871ab19334ad3d6666642834777440`  
		Last Modified: Mon, 16 Jun 2025 17:01:13 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a990984f400a942a705a6fdcf7085eb5208dc5c4bb00ee28d43149eae4618e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12020639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98ec7d24ae2fd24ae85ac68e926c15933606972f67aff8dbdefd3d43d9509c6`

```dockerfile
```

-	Layers:
	-	`sha256:138ee4a5418a46961fbb719f21969fcdef5019ae0a60f2b6a249917cf2a6add1`  
		Last Modified: Mon, 16 Jun 2025 19:48:22 GMT  
		Size: 12.0 MB (12008885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480974f87c503ea017d9f3ad42cc3ab8ab1d5b4a0659cd99055e2502f2e6c48f`  
		Last Modified: Mon, 16 Jun 2025 19:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250615.0.365905`

```console
$ docker pull archlinux@sha256:3f808d41e09261904a04709fc210a154ee56f6a9c369a15a70c2dfac5adab498
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250615.0.365905` - linux; amd64

```console
$ docker pull archlinux@sha256:00ddc0f2cdfa19e54f164037d768901f8fb81a1aa6a5b2907d259a6729be2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287711663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb635301b5860ac61bbf7aa404a7a2e5faa5f9b4aa967be5853c38db48f92f8e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f4798adc81b48051de112e7ae73136962449d8ea7e2ca5cdbcffd11241616ca6`  
		Last Modified: Mon, 16 Jun 2025 19:48:43 GMT  
		Size: 287.7 MB (287702494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a65be26e0401c45bc2b22a0dd51d271a1871ab19334ad3d6666642834777440`  
		Last Modified: Mon, 16 Jun 2025 17:01:13 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250615.0.365905` - unknown; unknown

```console
$ docker pull archlinux@sha256:a990984f400a942a705a6fdcf7085eb5208dc5c4bb00ee28d43149eae4618e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12020639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98ec7d24ae2fd24ae85ac68e926c15933606972f67aff8dbdefd3d43d9509c6`

```dockerfile
```

-	Layers:
	-	`sha256:138ee4a5418a46961fbb719f21969fcdef5019ae0a60f2b6a249917cf2a6add1`  
		Last Modified: Mon, 16 Jun 2025 19:48:22 GMT  
		Size: 12.0 MB (12008885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480974f87c503ea017d9f3ad42cc3ab8ab1d5b4a0659cd99055e2502f2e6c48f`  
		Last Modified: Mon, 16 Jun 2025 19:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:1a39198fcde68348c49a3fd78a54ced553af8168252c6222451f3fe943a4f7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:39f8172042016257f636967d77cfc11734cd9d5e372ad9489320706529ad96ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163047436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f454de10f672ef4f62e2ec1773bbdabb11673efa1b8c6ae2cd1efcf2e9447886`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2459e742a75074b2c8411917dea3d0e8805c859a8ffeb97721ec791c8a915fc2`  
		Last Modified: Mon, 16 Jun 2025 18:44:35 GMT  
		Size: 163.0 MB (163039096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd36e9a0c83950ba1c7fa16e989e8c15d85f200653423c255f1d591128e9c48`  
		Last Modified: Mon, 16 Jun 2025 17:09:40 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:7454d301fe6ce0b57517c165a887683b4a40c3a0d2313485df894f090790aa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb1b4194181934f13d3b3a417c67a4779cc5cc2b24c288f1a990af94e2ea662`

```dockerfile
```

-	Layers:
	-	`sha256:8c4c0334a3a3c5dc9750da23a7aac8b5a9a55b7ca5288d08fee25a9ef8fb34a8`  
		Last Modified: Mon, 16 Jun 2025 19:48:18 GMT  
		Size: 8.1 MB (8148072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038c36bba30c43529cbb600942ffd32f99d7f07b674a33145b056407f662548f`  
		Last Modified: Mon, 16 Jun 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:e287f123ab463a16b50a8f93dfeffce388f8898dd6b9c1d8cfc28720a8d7e69d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:92791803504f1ebdf65f9b56aefad77aeef1aa8b69bdd5f070298b605261c2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338883254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6317f7dd679b3721c19cf775bf51fd491293e33a85fa0229800db34da3165f8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:02e6014b6253d0bcfb75c2b6aa81578d274dfef6e38342a07c3502f8bee2c4dd`  
		Last Modified: Mon, 16 Jun 2025 20:11:27 GMT  
		Size: 338.9 MB (338872989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab38efd99beba1d1be334ad7e8804dd95e62583c7f473187d7784bc578a4d32`  
		Last Modified: Mon, 16 Jun 2025 17:01:40 GMT  
		Size: 10.3 KB (10265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:ba17fc0e373ca2be2678f77f748799214e3cefb2aed699ef753535a8f50cbb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12289585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66f4fd9b9c85f2affc34ebd402097507c8ef60f0b1df6cc490bea7e2424b077`

```dockerfile
```

-	Layers:
	-	`sha256:910f245c20451653c09fd19ccdb5ce3838380aef0acb63b36938c6672dfddb79`  
		Last Modified: Mon, 16 Jun 2025 19:48:26 GMT  
		Size: 12.3 MB (12277774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b719f3ec00f16e64314071de690f08d0d76f3d7d011dda316cf64c1f91419185`  
		Last Modified: Mon, 16 Jun 2025 19:48:27 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250615.0.365905`

```console
$ docker pull archlinux@sha256:e287f123ab463a16b50a8f93dfeffce388f8898dd6b9c1d8cfc28720a8d7e69d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250615.0.365905` - linux; amd64

```console
$ docker pull archlinux@sha256:92791803504f1ebdf65f9b56aefad77aeef1aa8b69bdd5f070298b605261c2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338883254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6317f7dd679b3721c19cf775bf51fd491293e33a85fa0229800db34da3165f8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:02e6014b6253d0bcfb75c2b6aa81578d274dfef6e38342a07c3502f8bee2c4dd`  
		Last Modified: Mon, 16 Jun 2025 20:11:27 GMT  
		Size: 338.9 MB (338872989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab38efd99beba1d1be334ad7e8804dd95e62583c7f473187d7784bc578a4d32`  
		Last Modified: Mon, 16 Jun 2025 17:01:40 GMT  
		Size: 10.3 KB (10265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250615.0.365905` - unknown; unknown

```console
$ docker pull archlinux@sha256:ba17fc0e373ca2be2678f77f748799214e3cefb2aed699ef753535a8f50cbb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12289585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66f4fd9b9c85f2affc34ebd402097507c8ef60f0b1df6cc490bea7e2424b077`

```dockerfile
```

-	Layers:
	-	`sha256:910f245c20451653c09fd19ccdb5ce3838380aef0acb63b36938c6672dfddb79`  
		Last Modified: Mon, 16 Jun 2025 19:48:26 GMT  
		Size: 12.3 MB (12277774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b719f3ec00f16e64314071de690f08d0d76f3d7d011dda316cf64c1f91419185`  
		Last Modified: Mon, 16 Jun 2025 19:48:27 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
