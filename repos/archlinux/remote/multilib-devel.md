## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:381838703ee564e8e7a29cca049c72b304bc6ff83c3a5f12d1c783f7c50566de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:511ccee2464ee5da2cdb1b99a24c9538a5c32d13289d7b59893d104af0995148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324062556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e2370fef6a51b2636be8f4a3fc6661118df4b39f4c54365a1ddecfb49321ce`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35f18d87fe1c34fb6189104a5557fc7dd308f8df7e0bb81cf374e2a2d3b7c8a2`  
		Last Modified: Tue, 07 Jan 2025 01:30:06 GMT  
		Size: 324.1 MB (324052296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4777a9c61f77fa4ba01d232c41a281a4f2669416dcf2a966ee788a7d60bf0307`  
		Last Modified: Tue, 07 Jan 2025 03:15:03 GMT  
		Size: 10.3 KB (10260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:7f9ecef7e3853105e82c3de3d19ef23318211a3656ba9bdd4cbf3a8a50b26ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208881dde28c504e4b93a5345dd6718dfbbe15eeff035120208988ed52cb1fa6`

```dockerfile
```

-	Layers:
	-	`sha256:957597259501490e469c8418ee89c128a9621ed33c5fa52137a2321b4a9c442a`  
		Size: 12.2 MB (12164822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d12b515b47b52b249bb9e07785903d76faa1762d42281a49d36b1ce792e9870`  
		Last Modified: Tue, 07 Jan 2025 03:15:03 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
