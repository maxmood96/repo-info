## `archlinux:base`

```console
$ docker pull archlinux@sha256:40ec92af4b7de7127251038f2e1af7978c1dbc1625e4c7d23b7a89eee05e5a58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:ca64cafd0d2e1fd5744d0f607f11a0b33be173790665c9e2931f756ffbb0a37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131712404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd549cf9ec5dc1c2a348412027a9b3bde3d5ed00698c23c7e24b0f9f16eefef`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.version=20260524.0.535079
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Tue, 26 May 2026 18:59:31 GMT
LABEL org.opencontainers.image.created=2026-05-24T00:12:57+00:00
# Tue, 26 May 2026 18:59:31 GMT
COPY /rootfs/ / # buildkit
# Tue, 26 May 2026 18:59:33 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260524.0.535079' /etc/os-release # buildkit
# Tue, 26 May 2026 18:59:33 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 18:59:33 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7e3ad9f3b68bf3c61b23f847702a58c98f1475ba219c285f7bf497551fb36f9`  
		Last Modified: Tue, 26 May 2026 18:59:59 GMT  
		Size: 131.7 MB (131703722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d633867c6969f24ab449103f26513eb33bc780f1566a72329f116d418cc54bc1`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 8.7 KB (8682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:880c90ec7e95b7cc9fc6ab5292ec96200fe58b7c6a8a2f803d0c8ef7b6a38238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fff2f70ac70fb49234ecc8f90ad340573e13c497911207a21643c14ffdad6e`

```dockerfile
```

-	Layers:
	-	`sha256:c9e51910311b5b0a345291c8a183f27420ebe6410fcc6e29b87f18ac614c32e2`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 8.2 MB (8181157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6ead6609704b294727cc86e83a37930b390b63cb33b0a48dabffc75fc251c8`  
		Last Modified: Tue, 26 May 2026 18:59:56 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json
