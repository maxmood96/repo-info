## `archlinux:multilib-devel-20260412.0.513370`

```console
$ docker pull archlinux@sha256:f9b793d23b89cb123c643aa2106744ddc0142d185d3d5a7749887cb3d046826a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260412.0.513370` - linux; amd64

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

### `archlinux:multilib-devel-20260412.0.513370` - unknown; unknown

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
