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
