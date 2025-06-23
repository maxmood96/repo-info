## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:528e9633b78ea2c2044b58b61199b00f7c05484ceaaf38ce6365a6171bf5a12f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:80530de0623809411a822facba5b22bd4eac34ec03c732a8050d425ba41a7491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338895365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e65f705ba451809814adbd5372ab385234a15dc1b21f0bef0a6efb036d1c2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250622.0.370030
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-06-22T00:07:28+00:00
# Sun, 22 Jun 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250622.0.370030' /etc/os-release # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Jun 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c0d08995da1c28452b383d3dd1b586f235d9e3d8ec35ee5ff1507e5a330cfdad`  
		Last Modified: Mon, 23 Jun 2025 19:52:32 GMT  
		Size: 338.9 MB (338885115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10dd6e569b7f68cf63e3e269781f893165a9cf721b6a4a8331edfc5c5666e81`  
		Last Modified: Mon, 23 Jun 2025 16:53:06 GMT  
		Size: 10.2 KB (10250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:4b78d5ff04c410cf8d98378c130eccf537b2b637bb6f4098f718549019264fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12290307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d6d9432cb34441f7414593c39402badc2e1f4511e0a2925f347fcbb3af9562`

```dockerfile
```

-	Layers:
	-	`sha256:72a9faa471318afefcfc7057379d2082101f9a0316b542cd757ff4e8334b3e09`  
		Last Modified: Mon, 23 Jun 2025 19:48:25 GMT  
		Size: 12.3 MB (12278496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25d77b6846e61c76fdfaec27f583f74f3e43254962023bb9423b16d9abf96d`  
		Last Modified: Mon, 23 Jun 2025 19:48:26 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
