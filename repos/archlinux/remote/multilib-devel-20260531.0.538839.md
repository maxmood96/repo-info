## `archlinux:multilib-devel-20260531.0.538839`

```console
$ docker pull archlinux@sha256:ac45720cd4e51daff8f164699bc83662386e5247906b78e85098de210de6c839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260531.0.538839` - linux; amd64

```console
$ docker pull archlinux@sha256:5acd74e1ec80246e5428e9fb833109555b9981629ec8fd30ea39863528b1c174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326397104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1700b1308251bd3b3753f8e2397827d22b5ba0220c2cd0fb076eab011efbd0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:31:06 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:31:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:31:13 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:31:13 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:31:13 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:183d3e1c43c83600bb5f00d3fabd0bca7e80c7e5db7c5c49f6ec47c8d31a1f4c`  
		Last Modified: Mon, 01 Jun 2026 21:32:19 GMT  
		Size: 326.4 MB (326384561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e75021c7a376af5d4ed3aca9430442b41fcc90e6e5a08975482a8de7cc2a47`  
		Last Modified: Mon, 01 Jun 2026 21:32:06 GMT  
		Size: 12.5 KB (12543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260531.0.538839` - unknown; unknown

```console
$ docker pull archlinux@sha256:44afef308412338fa806f5bc52fe5b5de07c28bdb63c1898c77937230b6b591a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14667097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2079080fdf437c5239e148a040778f51f10fb063a6552141a884653c4589a5`

```dockerfile
```

-	Layers:
	-	`sha256:253edf92189c79a07ccb7f655585add73cb8aa0577e836a5d6338d88a7bfa25f`  
		Last Modified: Mon, 01 Jun 2026 21:32:07 GMT  
		Size: 14.7 MB (14655329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f93ca7905912e7fb1d25286b614911069966a4eaf3fa3c0cb0a07133130890`  
		Last Modified: Mon, 01 Jun 2026 21:32:06 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
