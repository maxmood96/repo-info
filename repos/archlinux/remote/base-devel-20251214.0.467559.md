## `archlinux:base-devel-20251214.0.467559`

```console
$ docker pull archlinux@sha256:9414f5b766a34ebd769608b9ec80e1b4bfd7ea5e86dd49cae06ae308ad6c4221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251214.0.467559` - linux; amd64

```console
$ docker pull archlinux@sha256:e70875c9b4d9255ca79874fb4ea44a635786e6029f130ee4aa1ba4fe583eab5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4633b6c477df051bc51c08ae1f6409f12ebe939c41d02f71d544b3fa14b197b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:28:57 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:29:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:29:04 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:28f03c6e8bb3a7030933065fad15d28b50b0bfc498ea6d4cedd92904feb81e22`  
		Last Modified: Mon, 15 Dec 2025 18:33:53 GMT  
		Size: 292.1 MB (292061547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec6827e8076675e684a976065d24343ac4e4526b572e6fc2fac4f4f4bc9e13f`  
		Last Modified: Thu, 18 Dec 2025 00:29:57 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251214.0.467559` - unknown; unknown

```console
$ docker pull archlinux@sha256:d2d7cd076c4272924466ed1ea4ed4313bb018e888c6fa6392bca372a5ed90d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12142872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92432e93531d948c726d191ad80db451daba2730389a263533b13a0c978e2016`

```dockerfile
```

-	Layers:
	-	`sha256:270abacd820fb98a36d2ac78e0a917a713abf3c021771795b148c556408dffb7`  
		Last Modified: Thu, 18 Dec 2025 02:48:22 GMT  
		Size: 12.1 MB (12131161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ccbcee7b05649d682c72ab32235add143982b403be4f0be2a265ebdf79c014`  
		Last Modified: Thu, 18 Dec 2025 02:48:23 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
