## `archlinux:base`

```console
$ docker pull archlinux@sha256:1a39198fcde68348c49a3fd78a54ced553af8168252c6222451f3fe943a4f7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:39f8172042016257f636967d77cfc11734cd9d5e372ad9489320706529ad96ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163047436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f454de10f672ef4f62e2ec1773bbdabb11673efa1b8c6ae2cd1efcf2e9447886`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2459e742a75074b2c8411917dea3d0e8805c859a8ffeb97721ec791c8a915fc2`  
		Last Modified: Mon, 16 Jun 2025 18:44:35 GMT  
		Size: 163.0 MB (163039096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd36e9a0c83950ba1c7fa16e989e8c15d85f200653423c255f1d591128e9c48`  
		Last Modified: Mon, 16 Jun 2025 17:09:40 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:7454d301fe6ce0b57517c165a887683b4a40c3a0d2313485df894f090790aa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb1b4194181934f13d3b3a417c67a4779cc5cc2b24c288f1a990af94e2ea662`

```dockerfile
```

-	Layers:
	-	`sha256:8c4c0334a3a3c5dc9750da23a7aac8b5a9a55b7ca5288d08fee25a9ef8fb34a8`  
		Last Modified: Mon, 16 Jun 2025 19:48:18 GMT  
		Size: 8.1 MB (8148072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038c36bba30c43529cbb600942ffd32f99d7f07b674a33145b056407f662548f`  
		Last Modified: Mon, 16 Jun 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
