<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260419.0.517065`](#archlinuxbase-202604190517065)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260419.0.517065`](#archlinuxbase-devel-202604190517065)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260419.0.517065`](#archlinuxmultilib-devel-202604190517065)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:5ba8bb318666baef4d33afefc0e65db80f38b23503cb8e7b150d315cc2d4d5da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:52c1b90e0bdffda8bac47c8cf87c5a1883b184fe3513b395f7983559766f9625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129464186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26b5ec8ec89a92d0189a76aa40a864b8c70f9a6feb1353c45b3d85981c3629f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:46:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:46:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1dd624a5d250d23d3790c8017dc38ec1c1abcba105a256f751dd76fefead5bd0`  
		Last Modified: Mon, 20 Apr 2026 21:46:40 GMT  
		Size: 129.5 MB (129455522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ef42a20b3561e23c409877f7f8f4b01e22f927b8755bfc78b5e24a5e9cce5`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:b1a9bba7b891358f6a6351b0d65e578aa9df0229f651cce7f4ae85a1d6b699c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8191391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f512ec2e652487772d147d875364fffeb1c6ed5cc06142df92e2b2d33f387ce7`

```dockerfile
```

-	Layers:
	-	`sha256:e34c7f2f1ce4b7c8f2bd54890f6793e9e45a4676ecf53896dbedfa68c21013f6`  
		Last Modified: Mon, 20 Apr 2026 21:46:38 GMT  
		Size: 8.2 MB (8179463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a766b74985a817edc43640c780b0dccfc7acb8f393cdd2da70f149d1a91cfc06`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260419.0.517065`

```console
$ docker pull archlinux@sha256:5ba8bb318666baef4d33afefc0e65db80f38b23503cb8e7b150d315cc2d4d5da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260419.0.517065` - linux; amd64

```console
$ docker pull archlinux@sha256:52c1b90e0bdffda8bac47c8cf87c5a1883b184fe3513b395f7983559766f9625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129464186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26b5ec8ec89a92d0189a76aa40a864b8c70f9a6feb1353c45b3d85981c3629f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:46:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:46:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1dd624a5d250d23d3790c8017dc38ec1c1abcba105a256f751dd76fefead5bd0`  
		Last Modified: Mon, 20 Apr 2026 21:46:40 GMT  
		Size: 129.5 MB (129455522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ef42a20b3561e23c409877f7f8f4b01e22f927b8755bfc78b5e24a5e9cce5`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260419.0.517065` - unknown; unknown

```console
$ docker pull archlinux@sha256:b1a9bba7b891358f6a6351b0d65e578aa9df0229f651cce7f4ae85a1d6b699c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8191391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f512ec2e652487772d147d875364fffeb1c6ed5cc06142df92e2b2d33f387ce7`

```dockerfile
```

-	Layers:
	-	`sha256:e34c7f2f1ce4b7c8f2bd54890f6793e9e45a4676ecf53896dbedfa68c21013f6`  
		Last Modified: Mon, 20 Apr 2026 21:46:38 GMT  
		Size: 8.2 MB (8179463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a766b74985a817edc43640c780b0dccfc7acb8f393cdd2da70f149d1a91cfc06`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c528201c37821ac7883af233a18eba79fbce9bd900aeae07462888a607741abe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5d566859254d6e7bab01fe4c84b3c34225635fd7325997a20d1dcfe070ec4012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247090930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d6752db797d0c58355267abfc01676c4de55605ea4e0347eec28521d2bbe0c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Wed, 15 Apr 2026 20:13:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:13:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Wed, 15 Apr 2026 20:13:35 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:13:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5c1f30f5a8968675635fdbe2ce53d92208401558240cf52fcdaf22993ac0aaca`  
		Last Modified: Mon, 13 Apr 2026 17:49:09 GMT  
		Size: 247.1 MB (247081762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523280c44e7faa57b0d2d5cb35be382177a90d8c331dce34893b214ad76af178`  
		Last Modified: Wed, 15 Apr 2026 20:14:17 GMT  
		Size: 9.2 KB (9168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8218774c140b512b8b4219cdd5bb256b040b058c6e4fe4edf98f93a0a7a257f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11976487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acd59f8199b91219b75287adad2a4a589c4d8de00018d6f68bebc8008fbf5e9`

```dockerfile
```

-	Layers:
	-	`sha256:89280d33137b311d2821b31e2d98fb36ed029f6436f92adc22e4fed1ad4370cd`  
		Last Modified: Wed, 15 Apr 2026 20:14:17 GMT  
		Size: 12.0 MB (11964776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756b40acbb75c4ba1965694c098d12de89622ca535b5fcd6d7a079ce52123bb2`  
		Last Modified: Wed, 15 Apr 2026 20:14:17 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260419.0.517065`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:5ba8bb318666baef4d33afefc0e65db80f38b23503cb8e7b150d315cc2d4d5da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:52c1b90e0bdffda8bac47c8cf87c5a1883b184fe3513b395f7983559766f9625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129464186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26b5ec8ec89a92d0189a76aa40a864b8c70f9a6feb1353c45b3d85981c3629f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:46:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:46:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1dd624a5d250d23d3790c8017dc38ec1c1abcba105a256f751dd76fefead5bd0`  
		Last Modified: Mon, 20 Apr 2026 21:46:40 GMT  
		Size: 129.5 MB (129455522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ef42a20b3561e23c409877f7f8f4b01e22f927b8755bfc78b5e24a5e9cce5`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:b1a9bba7b891358f6a6351b0d65e578aa9df0229f651cce7f4ae85a1d6b699c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8191391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f512ec2e652487772d147d875364fffeb1c6ed5cc06142df92e2b2d33f387ce7`

```dockerfile
```

-	Layers:
	-	`sha256:e34c7f2f1ce4b7c8f2bd54890f6793e9e45a4676ecf53896dbedfa68c21013f6`  
		Last Modified: Mon, 20 Apr 2026 21:46:38 GMT  
		Size: 8.2 MB (8179463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a766b74985a817edc43640c780b0dccfc7acb8f393cdd2da70f149d1a91cfc06`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:f9b793d23b89cb123c643aa2106744ddc0142d185d3d5a7749887cb3d046826a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:504a56aed69d537dbc4713fcdf13e9e228640d4bb840dc98f4e4a1ef17d4bcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269252304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8d318d707c4570e74f786b911c178bc841b653ccd53d654fd43c6948d13e5c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Wed, 15 Apr 2026 20:14:48 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:14:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Wed, 15 Apr 2026 20:14:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58f17d36b1f875da33d63bcf8aca97555ff01fd66e8541aa5ba8046f40f02bde`  
		Last Modified: Mon, 13 Apr 2026 17:49:04 GMT  
		Size: 269.2 MB (269241935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6715389c3c30f1c8a355b1df8f844c5e3dacb1ddc36f042bd90533848d9cc95d`  
		Last Modified: Wed, 15 Apr 2026 20:15:39 GMT  
		Size: 10.4 KB (10369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:85e7aa73ed5ebd91b18de8e0841c0fe40ef5cf338b692bd7015a739c7ffdad7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12246414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8822b03ae05742dd5f83f716bd647976bda299429cc2d002728f84cab6f9e3b5`

```dockerfile
```

-	Layers:
	-	`sha256:a02d7474b59935c8137e1e12f105713ac8f714f88fa0cd4ca0dc9eead32fe78f`  
		Last Modified: Wed, 15 Apr 2026 20:15:40 GMT  
		Size: 12.2 MB (12234646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf76508a559f2e70a7f6b6853ce6471268959406b5ca1e7a9fcbca9b62e9799`  
		Last Modified: Wed, 15 Apr 2026 20:15:40 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260419.0.517065`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
