## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:11ce6b24090cb1b5025231b17ab50d144c03612d740224ca3d83a761df120939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0d2ae0be60686321b490b57c9cb90c3f2d64eeb05ffeac4c2faa01907cd72777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293785552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a7e1d583d418cbc0c4eec787b2158a08cb9864c28d36a7792105ea62b964bf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:36:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:36:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:36:57 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:36:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1e89069645e551320191d6ed4f9c08c6914dfd1f3290113122c929bd19065ebc`  
		Last Modified: Mon, 26 Jan 2026 19:37:49 GMT  
		Size: 293.8 MB (293776194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02de33fa295f4b98e030eaec091ef6268afb810d40301ba72f06e3e614f291e7`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:243a1cea567a7f054214e2a5bb0567dc7690980ed60051094b539a8d43691eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bf232cf77f577f1468bde3b59ded88c6497bf2441410b2aa1fb9379db05418`

```dockerfile
```

-	Layers:
	-	`sha256:bb6361dfa11d7e7f02840f746ca77831a128aaa0c4e41ad524cc97b5d3fe5527`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c00a06ef49317dbc918b98288ce7d44c43151e37138212b01e2df96f388be3`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
