## `archlinux:latest`

```console
$ docker pull archlinux@sha256:ca6af8049bd9dee3eb2bc3d620642ca1bc81b00f10aa08b12ee28ac56063be49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:a8904aee9b0599e9b0497d49195dfb8beb94b3c01a7bb56ec18168143f810655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165272328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a450996096cb455fccd0e5fd50f9c5390ee1c1f4e7f390b9a90ec74281549d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f76ba238a84a63b71e658023be058526928f3de0dcb19747c2a10d5a20567f04`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 165.3 MB (165263996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afbbb9519488fa765e35f101d286e1fb1e617085d1373cb282b33fa59079619`  
		Last Modified: Mon, 06 Oct 2025 18:07:47 GMT  
		Size: 8.3 KB (8332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:f072fbe3c36425cecfa820b581547be2571cb1f536a8747e276a4c3644803838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8230220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37929c702aa964aa6174ed85bf6006a935a4cac62fd9923e03b7a333df204396`

```dockerfile
```

-	Layers:
	-	`sha256:ad85159e1193664cb877e2ffd5521402aca2b5a192629369fe964608538ef30a`  
		Last Modified: Mon, 06 Oct 2025 19:48:19 GMT  
		Size: 8.2 MB (8218248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae50ed92a734e6ec6d3600faf7f79848c408da8b56946cdbb50a59677c2a5182`  
		Last Modified: Mon, 06 Oct 2025 19:48:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
