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
