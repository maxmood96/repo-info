## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:62b48a4626012151d9ee4af09327960544705347c1a5d7fc1b201e6cb6c68a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0755415f74a28c1929b1943844e3ee61fc56b7c184adb0520c3fcc296aa5524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345103912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a82e0671c48eb44cbf77019aa289814255fe288e4cf72e2d90232cf075bf89f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:15:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:15:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b082aaf37d1f8448ecdf12a68276aa8babba8acde9f2d22a3396b4db41c0684d`  
		Last Modified: Mon, 26 Jan 2026 19:37:38 GMT  
		Size: 345.1 MB (345093462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b9c8e8e1cf6559d71b9af774ae973e20cff63e99786d53a47af30139ee2b9`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a23a2753526a42201223973ccc77d6c5c1717d0df974080445005859a1b508bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12442784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2780033282d205047f48551a33524b2ecb8776b9b25acd6206a42b2e920d3cf`

```dockerfile
```

-	Layers:
	-	`sha256:43f3a03a18066722189daa2d4482e24262a4c8fa5406bd0454c0aabf9b7201b6`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 12.4 MB (12431019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44cb6afc2af36a9e94721f186ccc689077d74a4dc38a8306a62d73c53826f80`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json
