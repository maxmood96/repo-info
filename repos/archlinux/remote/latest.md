## `archlinux:latest`

```console
$ docker pull archlinux@sha256:d9abf957599bddf27955a0dd82b4457dcfaace50525bb773f6c7518f8015e7e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:cc54f12fae7c81bd0d1a38f1694b4c28ffc708b358dd5876ab77dde49d37925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131368828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435ed19930af3ee3bbecbface47941c8fd2a6e3985516ceeb61d2b3b3e78ab09`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.version=20260621.0.546891
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.created=2026-06-21T00:09:09+00:00
# Mon, 22 Jun 2026 19:45:05 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 19:45:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260621.0.546891' /etc/os-release # buildkit
# Mon, 22 Jun 2026 19:45:07 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:45:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ab5bfa2e5807a3c5c29f3e1ca9c37088a006dd7a0b85eaf01292209d76ecc57b`  
		Last Modified: Mon, 22 Jun 2026 19:45:32 GMT  
		Size: 131.4 MB (131360138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b870649fd58e8b1d400a4293bb484d7f462a736493ce0ac56fd2faa68f38ca8`  
		Last Modified: Mon, 22 Jun 2026 19:45:29 GMT  
		Size: 8.7 KB (8690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:5023748da22f12ddc65821a144a7105c4d8cfd3a3926f021c82f3a27430b9ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8188301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65147f82d924d8f4af76fbbcc29ba1bcdc2e038bcf1464488fd31d86cf37864`

```dockerfile
```

-	Layers:
	-	`sha256:001bafb1448cc60f0138f0068135b43fffb51a1bcdf6e408e28729ba3d3443ce`  
		Last Modified: Mon, 22 Jun 2026 19:45:29 GMT  
		Size: 8.2 MB (8176372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57e136ab266c57d7367c6134d5c3b6902eaf48ca82ea294cc14edd30bd1f092`  
		Last Modified: Mon, 22 Jun 2026 19:45:28 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
