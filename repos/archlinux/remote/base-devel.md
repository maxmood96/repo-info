## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c26263d698029443e20a4dcfa26d4c7180216f28fa5dbe6a6c12f8f031dc757b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:354f88d30991e6d9a7dcd831fda1983701fe7c4b40cfd8b2b8b29ff4b41177a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293785552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7612e886c56dc6d1a291b346986b51af2362f38280bf81ff22a9f0d2d34f9b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:13:46 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:13:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:13:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1e89069645e551320191d6ed4f9c08c6914dfd1f3290113122c929bd19065ebc`  
		Last Modified: Mon, 26 Jan 2026 19:37:49 GMT  
		Size: 293.8 MB (293776194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316601f3a3fb10987a7d2a44b0e4251175abf717727a7391499227120e07029f`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3cdc30e26f2f1c634cedcab1c3431efbc51d32a40019eb40794e736c483a65f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098dd36798168957b53dd47921b550a4bf4402311225af1d477d0e8ec4678d89`

```dockerfile
```

-	Layers:
	-	`sha256:c96eb7a7d902d72e3ab09d6292f560b31f626eee765fd62443d43963667be31f`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05314a8379a20655073273bc14a6baf271a4585b4d8ea3c952bdf5ea5526565`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json
