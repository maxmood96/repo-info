<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260208.0.488728`](#archlinuxbase-202602080488728)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260208.0.488728`](#archlinuxbase-devel-202602080488728)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260208.0.488728`](#archlinuxmultilib-devel-202602080488728)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:644b416048d39616bbaca93ce768ba492655c83fba80ceca65a4f59dcabdcac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:901ce548a325fe7cec8895e5837343af9c8ec89edb420d3a96b2cc6f5e86c771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176684514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bd5aa142840790b05c0cd1cfd1a2f45f027f26a821c992efb9e83f04956c10`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:34:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:34:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:34:54 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:34:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2efc828fc4c1e8872ffc2e6302cc5e768e96b0c007f65ca96fda719e3926c471`  
		Last Modified: Mon, 09 Feb 2026 19:35:24 GMT  
		Size: 176.7 MB (176675766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92388da7a721ababcdfa711244fe175254c409e8ec45b989a260e040ac66de2`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:f116c06fbb3b80b9a67e514e433887fd39d59a47bd78f76c1a98b0eaef5f4914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8416418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7480c9ee28ee5c453d165ffaadfebba1c72a33a47d386656cd15589377306a61`

```dockerfile
```

-	Layers:
	-	`sha256:999756a439ced73a1fc9afa4c48923466350a0ffd2850efa2aa8ffb00eb067c8`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 8.4 MB (8404489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77473698ebeedd394103e94dde7256d5b49922a8e6bd9e398969798f7b1b505`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260208.0.488728`

```console
$ docker pull archlinux@sha256:644b416048d39616bbaca93ce768ba492655c83fba80ceca65a4f59dcabdcac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260208.0.488728` - linux; amd64

```console
$ docker pull archlinux@sha256:901ce548a325fe7cec8895e5837343af9c8ec89edb420d3a96b2cc6f5e86c771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176684514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bd5aa142840790b05c0cd1cfd1a2f45f027f26a821c992efb9e83f04956c10`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:34:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:34:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:34:54 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:34:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2efc828fc4c1e8872ffc2e6302cc5e768e96b0c007f65ca96fda719e3926c471`  
		Last Modified: Mon, 09 Feb 2026 19:35:24 GMT  
		Size: 176.7 MB (176675766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92388da7a721ababcdfa711244fe175254c409e8ec45b989a260e040ac66de2`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260208.0.488728` - unknown; unknown

```console
$ docker pull archlinux@sha256:f116c06fbb3b80b9a67e514e433887fd39d59a47bd78f76c1a98b0eaef5f4914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8416418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7480c9ee28ee5c453d165ffaadfebba1c72a33a47d386656cd15589377306a61`

```dockerfile
```

-	Layers:
	-	`sha256:999756a439ced73a1fc9afa4c48923466350a0ffd2850efa2aa8ffb00eb067c8`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 8.4 MB (8404489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77473698ebeedd394103e94dde7256d5b49922a8e6bd9e398969798f7b1b505`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:7c81df532d6307c5bccb3d2561c90bfc981e6c4384d2a61c9e49b7f2d8aa27c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d8a877440f606a0e21e908a03b2df5cb906b73ba0337a7bdedb03970c479a845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.2 MB (294203152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111c89e8968bc4f51cbc12a62517b9d96682e4a2375610cfcc00a86f3b8fa57`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:35:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:36:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:36:04 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:36:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:97e9952b1492752f4f71887e07845b186f90b45b9dc4ae9e39c30a3a1536a391`  
		Last Modified: Mon, 09 Feb 2026 19:36:54 GMT  
		Size: 294.2 MB (294193801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10846ad6040d4843c966852be4dc2ff6e06f566e4cf7ed435fa1c9581e85cae6`  
		Last Modified: Mon, 09 Feb 2026 19:36:47 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:29788cd3eca690fb9232c66c9264e7585becf98ab1ef3595133412500b6eec93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12178525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596909a6d2cc347bdf93d21c81b380c0019a0571d794d1b15ee6ebd61cc47286`

```dockerfile
```

-	Layers:
	-	`sha256:c137a5fc54d78f1afc7e673b0bded8c21f6091f7aa1cc44fbf0b20e9b629eb9a`  
		Last Modified: Mon, 09 Feb 2026 19:36:47 GMT  
		Size: 12.2 MB (12166814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475ca361cd9b874b983ce000e7a1b887573a50d357418610cf4c74497672307f`  
		Last Modified: Mon, 09 Feb 2026 19:36:47 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260208.0.488728`

```console
$ docker pull archlinux@sha256:7c81df532d6307c5bccb3d2561c90bfc981e6c4384d2a61c9e49b7f2d8aa27c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260208.0.488728` - linux; amd64

```console
$ docker pull archlinux@sha256:d8a877440f606a0e21e908a03b2df5cb906b73ba0337a7bdedb03970c479a845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.2 MB (294203152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111c89e8968bc4f51cbc12a62517b9d96682e4a2375610cfcc00a86f3b8fa57`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:35:57 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:35:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:36:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:36:04 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:36:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:97e9952b1492752f4f71887e07845b186f90b45b9dc4ae9e39c30a3a1536a391`  
		Last Modified: Mon, 09 Feb 2026 19:36:54 GMT  
		Size: 294.2 MB (294193801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10846ad6040d4843c966852be4dc2ff6e06f566e4cf7ed435fa1c9581e85cae6`  
		Last Modified: Mon, 09 Feb 2026 19:36:47 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260208.0.488728` - unknown; unknown

```console
$ docker pull archlinux@sha256:29788cd3eca690fb9232c66c9264e7585becf98ab1ef3595133412500b6eec93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12178525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596909a6d2cc347bdf93d21c81b380c0019a0571d794d1b15ee6ebd61cc47286`

```dockerfile
```

-	Layers:
	-	`sha256:c137a5fc54d78f1afc7e673b0bded8c21f6091f7aa1cc44fbf0b20e9b629eb9a`  
		Last Modified: Mon, 09 Feb 2026 19:36:47 GMT  
		Size: 12.2 MB (12166814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475ca361cd9b874b983ce000e7a1b887573a50d357418610cf4c74497672307f`  
		Last Modified: Mon, 09 Feb 2026 19:36:47 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:644b416048d39616bbaca93ce768ba492655c83fba80ceca65a4f59dcabdcac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:901ce548a325fe7cec8895e5837343af9c8ec89edb420d3a96b2cc6f5e86c771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176684514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bd5aa142840790b05c0cd1cfd1a2f45f027f26a821c992efb9e83f04956c10`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:34:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:34:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:34:54 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:34:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2efc828fc4c1e8872ffc2e6302cc5e768e96b0c007f65ca96fda719e3926c471`  
		Last Modified: Mon, 09 Feb 2026 19:35:24 GMT  
		Size: 176.7 MB (176675766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92388da7a721ababcdfa711244fe175254c409e8ec45b989a260e040ac66de2`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:f116c06fbb3b80b9a67e514e433887fd39d59a47bd78f76c1a98b0eaef5f4914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8416418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7480c9ee28ee5c453d165ffaadfebba1c72a33a47d386656cd15589377306a61`

```dockerfile
```

-	Layers:
	-	`sha256:999756a439ced73a1fc9afa4c48923466350a0ffd2850efa2aa8ffb00eb067c8`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 8.4 MB (8404489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77473698ebeedd394103e94dde7256d5b49922a8e6bd9e398969798f7b1b505`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:223963305dfbb4a1a5ac46a12e87966526df053abe87dc4662eb1d512feaa435
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c2f8ab73bfeb71ca21edfd2613e96aeb4166835e5cc4139c12fafd0823f57b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345524666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1af8b22150e3f0d3732212ec0bdbe6e6cbd19468550ccf784b2f152e7e33958`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:37:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:37:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:37:40 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:37:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c87d276e83970850f8d41f0d5f9e2c96eb05df99ef0478d864e9e9b5a76ebd6c`  
		Last Modified: Mon, 09 Feb 2026 19:38:36 GMT  
		Size: 345.5 MB (345514244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571e13d7871681f45bbfef9522d1b4a8087420f777d1acb94f695bd1a01c2d2`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:aa971e7830192713f2819c672811cf73af8d9c0c76588ad3e86416c6e52ad302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12448457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c2e8a2bccce9cff0ecc1eeb863efd61d0c3b9e48c4a5889c458f23808c62cf`

```dockerfile
```

-	Layers:
	-	`sha256:fd0824790dbe8b02f896b98a6856502b7fa68f80694ffb58f28028124295f04e`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 12.4 MB (12436689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dfae207c8826eea78a0f6b07abfe3513d13120fd5239d616449287a7a417936`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260208.0.488728`

```console
$ docker pull archlinux@sha256:223963305dfbb4a1a5ac46a12e87966526df053abe87dc4662eb1d512feaa435
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260208.0.488728` - linux; amd64

```console
$ docker pull archlinux@sha256:c2f8ab73bfeb71ca21edfd2613e96aeb4166835e5cc4139c12fafd0823f57b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345524666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1af8b22150e3f0d3732212ec0bdbe6e6cbd19468550ccf784b2f152e7e33958`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:37:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:37:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:37:40 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:37:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c87d276e83970850f8d41f0d5f9e2c96eb05df99ef0478d864e9e9b5a76ebd6c`  
		Last Modified: Mon, 09 Feb 2026 19:38:36 GMT  
		Size: 345.5 MB (345514244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571e13d7871681f45bbfef9522d1b4a8087420f777d1acb94f695bd1a01c2d2`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260208.0.488728` - unknown; unknown

```console
$ docker pull archlinux@sha256:aa971e7830192713f2819c672811cf73af8d9c0c76588ad3e86416c6e52ad302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12448457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c2e8a2bccce9cff0ecc1eeb863efd61d0c3b9e48c4a5889c458f23808c62cf`

```dockerfile
```

-	Layers:
	-	`sha256:fd0824790dbe8b02f896b98a6856502b7fa68f80694ffb58f28028124295f04e`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 12.4 MB (12436689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dfae207c8826eea78a0f6b07abfe3513d13120fd5239d616449287a7a417936`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
