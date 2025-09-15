## `archlinux:base-devel-20250914.0.420821`

```console
$ docker pull archlinux@sha256:9019fd8b026064ee6bbbe3fe38686b058752a14b1a9960fd9048509ebd72b5f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250914.0.420821` - linux; amd64

```console
$ docker pull archlinux@sha256:c9d775751f4db6799ba3ea8dc5145bc55cc1a5a704668865a98a581889fa44ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289424783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ccfc6dc51b6f9e681e0af0d775d9c1d407ae4722ec29aec5e23b6ef013d7d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250914.0.420821
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-14T00:07:14+00:00
# Sun, 14 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250914.0.420821' /etc/os-release # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 14 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2c5033a95e457971d4d5938e5a753faa2114aabd3ffe3947ff3bfed3170b552f`  
		Last Modified: Mon, 15 Sep 2025 19:49:43 GMT  
		Size: 289.4 MB (289415608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e20e2a0f08d7d3640a21ce42ca13b73e7490729c837acae9fdd9cb2dad0c64c`  
		Last Modified: Mon, 15 Sep 2025 17:00:53 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250914.0.420821` - unknown; unknown

```console
$ docker pull archlinux@sha256:b411f2009b4dd0c9ede0afb7d91e56017c166feaf733b065445d2016e73e6d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12095909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c384adb2cf9337d34b130328723db5d2fcc1d4cba90f930eac73da1c7545edc6`

```dockerfile
```

-	Layers:
	-	`sha256:ac1519a6eca3b70b3d74866947aaf32063c01ab711c12551e1b42a6b77c7ed1c`  
		Last Modified: Mon, 15 Sep 2025 19:48:22 GMT  
		Size: 12.1 MB (12084155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed1f723b393e89ea25368da7bf228dd63e870edffdc24c2a339e05f1cc901d0`  
		Last Modified: Mon, 15 Sep 2025 19:48:23 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
