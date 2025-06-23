## `archlinux:base-devel-20250622.0.370030`

```console
$ docker pull archlinux@sha256:bb4464b24c12e523070bc5e70412e318843d1ff37494f11ddd7f12a623547636
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250622.0.370030` - linux; amd64

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

### `archlinux:base-devel-20250622.0.370030` - unknown; unknown

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
