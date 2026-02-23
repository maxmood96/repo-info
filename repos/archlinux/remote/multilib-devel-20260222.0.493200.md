## `archlinux:multilib-devel-20260222.0.493200`

```console
$ docker pull archlinux@sha256:04cf8b6ba729ca6b0200cca680f591aed6e8db390ffeec1590e0bd070bad949d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260222.0.493200` - linux; amd64

```console
$ docker pull archlinux@sha256:e91594a007d05ac9ec8e154f081de04b27e201c866089e55dd8684976bf21d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268016219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde8eecd7b98b8657c0c1cac0e144a7e7e6bcd5104cf75457cafa5d4a2c46be7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:52 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58cd36eecd001d27b8bf513e4b9a543677be2ff054040e13132e363d7f6654a6`  
		Last Modified: Mon, 23 Feb 2026 19:09:45 GMT  
		Size: 268.0 MB (268005913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b49d38f90bb447f1f7052b78cf5a8ba507a3a6ca6680d285602e0d70812b46`  
		Last Modified: Mon, 23 Feb 2026 19:09:38 GMT  
		Size: 10.3 KB (10306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260222.0.493200` - unknown; unknown

```console
$ docker pull archlinux@sha256:104334d3b43f9b92ff91d50d1cfddb594f3bcba0ca1e1fcc1177c8bfd089ac7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12521554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68eddcc66ba3e07caed4f554319ad54e6f86f38dad2bd2abcca7d3af54868db6`

```dockerfile
```

-	Layers:
	-	`sha256:43266162b2b02dbd96e1e6a770fe695a0f5190c367b1fe9bbd0f3142aab724ff`  
		Last Modified: Mon, 23 Feb 2026 19:09:39 GMT  
		Size: 12.5 MB (12509786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0672a7aeed50a24bcf674c64e0f0aa58ea4ef16df0261e810ab3c2bdd75610`  
		Last Modified: Mon, 23 Feb 2026 19:09:38 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
