## `archlinux:base`

```console
$ docker pull archlinux@sha256:417aa2d3e8e4cc8377360a94bf48ae1ed38e593cbecfcb34feb16d57e3efa1b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:f63269aa09e82c18fe3066ba08d4e3e3ca0563aea84fbb85b7f65b317482c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176196185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ead43a9bf672282b8fd0b2a2c07466c68b91f3127f069671fc7e17ad9ff4a2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:41:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:41:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:41:50 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:41:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1783afd91fdd549adee0628532122581a17d849598d0cdbd9b23ae3b1cb1916e`  
		Last Modified: Mon, 12 Jan 2026 19:42:51 GMT  
		Size: 176.2 MB (176187405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d004c9cbdd7a9fb79180b6da2bccf91ade2e8cfb91669a192ac3d2825d13d`  
		Last Modified: Mon, 12 Jan 2026 19:42:19 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:fae8a207785da31c23883139edd4bfa54edcaa3f6305d94b77d17f204facc0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3f9c7390f6917ebf1a7679af233d24433cef1f6714c8ea7f4ee7adff54d70`

```dockerfile
```

-	Layers:
	-	`sha256:27231ef966bb178feb0db4f8b55bf7a45a91eb790a729d88034788c579cfa664`  
		Last Modified: Mon, 12 Jan 2026 20:48:18 GMT  
		Size: 8.4 MB (8398809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195204be3a072f4cbe86788d1502198815347f1ffe91d60e9a29134a8778ffa6`  
		Last Modified: Mon, 12 Jan 2026 20:48:19 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
