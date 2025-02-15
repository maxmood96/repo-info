## `archlinux:base`

```console
$ docker pull archlinux@sha256:33ff44f3d1d18207c1bdc1bf5c4283541b7680bb60e3092e6973437e4e1c3927
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:2a006ed10836e49964826d6b310b169983bffd474917e02727342012f1b970c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157673353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957e6371bf45c26d24c8087e3945b87428edc053e2f9bbdd6dfb730c04cd31df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c4ce51beea9c3c5783dd11628e243d1c6679951a48f0168e07d67ad3ff6c26c7`  
		Last Modified: Mon, 10 Feb 2025 20:48:58 GMT  
		Size: 157.7 MB (157665076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b40c5e7a481307aa7619a8d87e35c219aa4561ba990a0966f3bc9d1a6010a`  
		Last Modified: Fri, 14 Feb 2025 23:48:48 GMT  
		Size: 8.3 KB (8277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:11255ef2bdd57c2286e5d2dc5db45080286b763ac8feb6d5377c86a2e42028be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f360b3630fdc7343d3d479d626edf4d0194ad46a4416718d7ebbe1cdd18db038`

```dockerfile
```

-	Layers:
	-	`sha256:07222cb7abfdd97a79eed85c16598f4c62e302a850f356cc607f4206f8a79d8c`  
		Last Modified: Fri, 14 Feb 2025 23:48:15 GMT  
		Size: 8.1 MB (8089059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd7a88f9cd0c9337150a73888c196eb9d6b87b2ceb65bd05a8ab52ac11fa19e`  
		Last Modified: Fri, 14 Feb 2025 23:48:15 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json
