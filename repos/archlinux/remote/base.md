## `archlinux:base`

```console
$ docker pull archlinux@sha256:068a765646e75e51fe5d544b0f95c85d0322d0a372659e9d5f10fb8402ca53f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:d41d768e81cac3bede426e294ac5b2c55ed4bf697698c0f13ddd86b911f7f260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132537200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfecaf404bacab06015241b0ef859fadd56a432e90a8a1afe85ae711064b02e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.version=20260628.0.549485
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 29 Jun 2026 19:08:08 GMT
LABEL org.opencontainers.image.created=2026-06-28T00:09:46+00:00
# Mon, 29 Jun 2026 19:08:08 GMT
COPY /rootfs/ / # buildkit
# Mon, 29 Jun 2026 19:08:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260628.0.549485' /etc/os-release # buildkit
# Mon, 29 Jun 2026 19:08:11 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jun 2026 19:08:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cbe7d739b4820a7988913bcd894e81d9f657edc581454eaa28e235edaa237ab4`  
		Last Modified: Mon, 29 Jun 2026 19:08:39 GMT  
		Size: 132.5 MB (132528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307b4573bcc6dbfb3498befdf48ad1688c41c4e8f14618adfc9a7d124f20dbc`  
		Last Modified: Mon, 29 Jun 2026 19:08:34 GMT  
		Size: 8.7 KB (8650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:9f5eac37450bbb717c8f6d9b6c93449c767c72f222b1d61b88a0bd0868ff947d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8222452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9f0524ef21299cfb524f7b0e37dad9968ee8563998eeeabe9dcb1ef52eb3d3`

```dockerfile
```

-	Layers:
	-	`sha256:8a16447ffc2389c3bd76eb49ed8c81d2023ed8b117ef02e0d40abb1bd364b190`  
		Last Modified: Mon, 29 Jun 2026 19:08:34 GMT  
		Size: 8.2 MB (8210523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f56d5ad22f159f7099ae9af8fc654198cd9bb933aa99c70ce4f1b9b7a4b6f9e`  
		Last Modified: Mon, 29 Jun 2026 19:08:34 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
