## `archlinux:base-devel-20260315.0.500537`

```console
$ docker pull archlinux@sha256:87c122fd99e648dc1a12536d181d40bd7a27ad3201c4bcfa55ccf219b42f4806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260315.0.500537` - linux; amd64

```console
$ docker pull archlinux@sha256:45fe50716152d2b7b43c3a781a2e4c428fd3005baa44b0c4caa59a5fa5dc050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245961571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f26d654f62f77eb5ff99540cddcfdaeeaa8fac2bfc0b97f2fad93e148a2475`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:43:29 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:43:29 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:43:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:43:35 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:43:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3485bafd682693abf8d3d75ec09212f3e00add355d8f933af56e0604c74bf8b7`  
		Last Modified: Mon, 16 Mar 2026 16:44:16 GMT  
		Size: 246.0 MB (245952441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf818bfbd63010b013834ec47da74e396b1251b8b683c4e1b5ea47923df84070`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 9.1 KB (9130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260315.0.500537` - unknown; unknown

```console
$ docker pull archlinux@sha256:e06f9147ba9772ca4731dfcd218eef782886558631cb16b4fb038e3ccf9391c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11898427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c2d3f915da1ee5ca5d36d89a677228a24b0bc30a0fb316c0d669573730e0de`

```dockerfile
```

-	Layers:
	-	`sha256:c01c53ed3e218067dd499756ff3f3622d1825080c2f239f03dc6385d23f80a65`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 11.9 MB (11886716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f626a3dcae723542bbb7474bba9ee161f4bcd4553aea29c849254942315aa90`  
		Last Modified: Mon, 16 Mar 2026 16:44:11 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
