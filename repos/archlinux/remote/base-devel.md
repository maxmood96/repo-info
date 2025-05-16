## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:880766de4e2961c425c6de1666ff852c59e0432fef12cbea7b8c678a80e80710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b9a97634ea0221aa1585a2737234acac0d2af78514c45c33529fd63c965d8807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287038782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905aab36193055ef8dad88ca20da1c3f3e4a4370aa2e807c6415e7a2354e01d3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250511.0.348143
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-05-11T00:07:38+00:00
# Sun, 11 May 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 May 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250511.0.348143' /etc/os-release # buildkit
# Sun, 11 May 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 11 May 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:dfd741f6c2c280c7836df3cd6f21735be091319b1d2cf5ac19cc6cb7ceb6c00e`  
		Last Modified: Tue, 13 May 2025 19:25:50 GMT  
		Size: 287.0 MB (287029581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd4e158398659e624ef7fd8c61e5620b7c82e6733e0653c4eabf1802bbc508e`  
		Last Modified: Tue, 13 May 2025 19:19:10 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0758f567102c007a21be0ef4532239688a67ac23925ba06fe47701faa22cfce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12038073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5970151c2af6f779f309f7b952aa5cd8d63816a9a4a67ee3b259bf43252e8d65`

```dockerfile
```

-	Layers:
	-	`sha256:028f2f8f298389d380d4c47dccb911c42d06e33ce8fefef2abb95428cc47aa97`  
		Last Modified: Fri, 16 May 2025 17:19:13 GMT  
		Size: 12.0 MB (12026319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f362015cdb894c9795483cd12bc58adc2bceed0b0a77c78e6bb4e9ae41832422`  
		Last Modified: Fri, 16 May 2025 17:19:12 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
