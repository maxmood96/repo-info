## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:ebcaeca69c4d416f848aedcd27fe224384fd506f86046526a5d49ec6d9e29db1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ead95833f3f1ed3c9091b46ad6cb5fb2d74059563ae2103a571dfb7b9dc3dac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292240275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08743ab9e023f5fb8785572404c676b3b08ba5688ffe56d3a8fdf33cd5fcf025`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:17:31 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:17:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:17:38 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:17:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:eb6edcde3302363203e3f39893a530aa11ed565f5ed4627a0d7e1f2000bf8ec5`  
		Last Modified: Mon, 05 Jan 2026 18:18:56 GMT  
		Size: 292.2 MB (292231101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0aac60a122f2991c855cdcd7e0d24ac09592fb1d27e166496c75bb58963e5`  
		Last Modified: Mon, 05 Jan 2026 18:18:46 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:b0fc54738d748505da84b1863693a0936ce40b53bab34e9f4ab584e2bda9110d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12157441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f95b3a321ddb4960b838cc642749398c97374a3d72aa8b71e2a6a3d16c36bd`

```dockerfile
```

-	Layers:
	-	`sha256:e46139c11b088c470d1b181ce963da28489c53bd9ed6574f73a09f6f99aabb19`  
		Last Modified: Mon, 05 Jan 2026 20:48:24 GMT  
		Size: 12.1 MB (12145730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ba6472061812c247ad8f6be05c64ab2fbd67e4a0a6290a411940dff9c7306b`  
		Last Modified: Mon, 05 Jan 2026 20:48:25 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
