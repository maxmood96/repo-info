## `archlinux:base-devel-20260614.0.544538`

```console
$ docker pull archlinux@sha256:0cf5eb78f8c3ddcdd7ccc3f9168328fb57ec6be0f83f501a0b2006590e0c92ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260614.0.544538` - linux; amd64

```console
$ docker pull archlinux@sha256:9f859aff8a280ca9fd04eb493229216bf38aa7d5ab7f0a8da5eae2885a20d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303370848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afeaeb37cbe13985fabab768e31358a1c7b09d741d09f12ed32ac9f1568fa70`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.version=20260614.0.544538
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.created=2026-06-14T00:09:34+00:00
# Mon, 15 Jun 2026 18:39:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Jun 2026 18:39:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260614.0.544538' /etc/os-release # buildkit
# Mon, 15 Jun 2026 18:39:41 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jun 2026 18:39:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d0e821d2e92139b70424f0af216f4ed56ce678c90db4835d7022c7c8fb46b266`  
		Last Modified: Mon, 15 Jun 2026 18:40:36 GMT  
		Size: 303.4 MB (303359441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d899506f0105cb067bf94d4bc4fdee5372012ed2139d2508497c9561226be7d6`  
		Last Modified: Mon, 15 Jun 2026 18:40:30 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260614.0.544538` - unknown; unknown

```console
$ docker pull archlinux@sha256:9d3c2dd314d40bc45bceeb1bdfbc45e36ec1f3785e7f166e7a87ec61158f7b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14397839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f65127bb6eca80a62fb048537dc1ea11b1ce19eb91d6c6bc531142eb3c4ebf`

```dockerfile
```

-	Layers:
	-	`sha256:2e4f559095ece592ffcf48f67286144b5a3f94ca29e6480d4cbbef5a89292fed`  
		Last Modified: Mon, 15 Jun 2026 18:40:31 GMT  
		Size: 14.4 MB (14386127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293a64317b1535e3d614b7a2c689143d67d18f157179ca2ebf4ec4efc1ba4121`  
		Last Modified: Mon, 15 Jun 2026 18:40:30 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json
