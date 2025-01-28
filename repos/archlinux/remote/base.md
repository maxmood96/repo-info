## `archlinux:base`

```console
$ docker pull archlinux@sha256:8b0a7d7e22c2e78539406a37ba2a1eb431d31981be3d76e076f517d3b62204d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:3bce2f83a6504ada72797778a769ba8d3d1dfc22f529c80ef8ba73906033ac26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157486191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b4b47ea315e849e965183f7691a33ebd5b2a9a16a3bca677463ac8087b32ba`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250126.0.301347
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-01-26T00:07:29+00:00
# Sun, 26 Jan 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250126.0.301347' /etc/os-release # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 26 Jan 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:67ec0c022815565d7434df4949e91e31f0de221cfd5be60326bd3df4048bf885`  
		Last Modified: Tue, 28 Jan 2025 01:28:38 GMT  
		Size: 157.5 MB (157477900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28369bbf0fedeaf566c85ca85f3b563ef91d294baec32cce66238189f7a7c91d`  
		Last Modified: Tue, 28 Jan 2025 01:28:34 GMT  
		Size: 8.3 KB (8291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:760d0e0ea4677a55c379f3978d7599763f695d4471e5f76cd61ece5408ee8a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cf857683f5d5bc17410b01b44c329d67b4aaf4caa929c1b8cfe201125897c7`

```dockerfile
```

-	Layers:
	-	`sha256:895a89443e98e48f33777a14ad0535ac71ca23f4acc0ec76f4286c9ee3e8a136`  
		Last Modified: Tue, 28 Jan 2025 01:28:35 GMT  
		Size: 8.1 MB (8088477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d732f7d3e033908e0b5cf56e98fc940200efeff41c24b93395b184124b79ae28`  
		Last Modified: Tue, 28 Jan 2025 01:28:34 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
