## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:5649fdf8c653154c63de0060d73374896442000449782df138cc59b25d1cfa50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ff211158b1cd8274f3bb9c1acf9b4168161ab56f160b3907c12d4c5134265d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276392393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6ed11403ee45267b87af765a2d8a70c009f9c580084564438c6215a4e882d8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.version=20260510.0.525573
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.created=2026-05-10T00:08:50+00:00
# Mon, 11 May 2026 20:59:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 11 May 2026 20:59:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260510.0.525573' /etc/os-release &&     true # buildkit
# Mon, 11 May 2026 20:59:12 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 20:59:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4fe2236d6036cbfee9f99ef331f485222aeb03985c18221fa01995136a88c822`  
		Last Modified: Mon, 11 May 2026 21:00:00 GMT  
		Size: 276.4 MB (276382020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fffb86b76bb626b28e556361bb2419fc9a6e2df10170906bf7a3a52202d8ee`  
		Last Modified: Mon, 11 May 2026 20:59:54 GMT  
		Size: 10.4 KB (10373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:ed33f8da54e0cb1b86cbc14c557eb9efc28d5765ae81d4b73dada291e16b714c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12318913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d4f0b7c493eb72e26740d1c9bc3ad6b3aec4e6db8c944f6920f8aa406b8647`

```dockerfile
```

-	Layers:
	-	`sha256:8f144e63e694b70b73393656fd5878787d571c0d3d74ba77e709c02f06157926`  
		Last Modified: Mon, 11 May 2026 20:59:55 GMT  
		Size: 12.3 MB (12307063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d019e227ac1e5a8d778de8b71114f66ad9a529ec2997bc9999c9993a44bde6`  
		Last Modified: Mon, 11 May 2026 20:59:54 GMT  
		Size: 11.8 KB (11850 bytes)  
		MIME: application/vnd.in-toto+json
