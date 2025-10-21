## `archlinux:base`

```console
$ docker pull archlinux@sha256:c136b06a4f786b84c1cc0d2494fabdf9be8811d15051cd4404deb5c3dc0b2e57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:34c848de96e5e94268710ef1b520acd7e6cd9ae49b77a62aaa28b9bcc0a38552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165329516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60cf1d6ee7e10c450ee32d39393589a76e84ad9f3c55e0a12c59d8a4b08a980`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.version=20251019.0.436919
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.created=2025-10-19T00:07:20+00:00
# Sun, 19 Oct 2025 00:07:20 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251019.0.436919' /etc/os-release # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
ENV LANG=C.UTF-8
# Sun, 19 Oct 2025 00:07:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a59b1e251b8568aff85b2ffb74ea2f9ed87fee3de7c0b9b3940b6ce56c9c7c13`  
		Last Modified: Mon, 20 Oct 2025 21:29:18 GMT  
		Size: 165.3 MB (165321179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b0775ea0f9481add0c91f4644ee5834b792b6aa0babf5e465a3574fe8c33a`  
		Last Modified: Mon, 20 Oct 2025 20:27:15 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:702233454069087682ba2484f6b71d8f5b6dc53bc5c6ddb5527812d3de218bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea91b6c1f070904eb2fc7f471a38e5ea9006153d0ccef14ac0e9787eb4667a3`

```dockerfile
```

-	Layers:
	-	`sha256:b0646ee5ed692207731c857b9ff1974741162fbbe56da1cb2756920f60aca691`  
		Last Modified: Mon, 20 Oct 2025 22:48:15 GMT  
		Size: 8.2 MB (8217645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c8b795adf8dede24ac62d32dcbddb0f637870b3afe6744b6d5d2bcc5e60faa`  
		Last Modified: Mon, 20 Oct 2025 22:48:16 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
