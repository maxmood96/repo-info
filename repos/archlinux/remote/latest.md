## `archlinux:latest`

```console
$ docker pull archlinux@sha256:9a72b5e3c1675683016cb065f513deea7c65836cb5bd22b88c89353098faa40f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:3da61078ff1ed4b4e85416bb9359652ee699d025893a206228a5914c89a9fb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164738114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82680043225b167c73b674f935dfd98729e50bec62d48fff0e4bef0014eb5c2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.version=20250928.0.426921
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.created=2025-09-28T00:07:11+00:00
# Sun, 28 Sep 2025 00:07:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250928.0.426921' /etc/os-release # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
ENV LANG=C.UTF-8
# Sun, 28 Sep 2025 00:07:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f38b8cce2f83b4db2c474585717a2fc37797d6f8e617ba3e29cfc367d9f0af7e`  
		Last Modified: Mon, 29 Sep 2025 17:30:34 GMT  
		Size: 164.7 MB (164729761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e90a4a68db40a24f4b026253e54ef9796ce4b45a04ad7ca427f27c354be8a5`  
		Last Modified: Mon, 29 Sep 2025 17:29:23 GMT  
		Size: 8.4 KB (8353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:2ebf6711bfac6763dc28207679bbac05ba17a528db7d0f74b17e58ab5b1b3ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8228979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c51fa7c6be72241641c887ac4af9f828e2e9091e0a904e8e1e2b1977336f042`

```dockerfile
```

-	Layers:
	-	`sha256:862a0310b99ea050019740c577a0245d00aba587c9667de4b97224fb3fce83ef`  
		Last Modified: Mon, 29 Sep 2025 19:48:18 GMT  
		Size: 8.2 MB (8217007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9784034e7d2ec88ba8358427ec73277584c1a319b5a64b1470f19c7ea825f3`  
		Last Modified: Mon, 29 Sep 2025 19:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
