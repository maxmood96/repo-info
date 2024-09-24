## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:a723bca84af8678ab536c40d801b2d3e924609eb94fdb68bded2429761d6c936
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e14758c423c552c92c1915cc0eae7b7dec1f02b1e8c6babade9e9faf91621696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272192548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0750879428a1e237572004e17750a9cb040e4156aa1fcfe30dd80bbfead10182`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240922.0.264758
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-22T00:07:28+00:00
# Sun, 22 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240922.0.264758' /etc/os-release # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d6abce642a08032becb5b773d22440c35b58ffd22f076691b2fa3ed896fe4c5a`  
		Last Modified: Tue, 24 Sep 2024 01:00:58 GMT  
		Size: 272.2 MB (272183552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aa93043ad97fe0ac219a3937b67a76fdd71063a8de1fb71ad7bb0ca7dc7693`  
		Last Modified: Tue, 24 Sep 2024 01:00:54 GMT  
		Size: 9.0 KB (8996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f118252b285cedf3f562e9bc839fd22fab98ae5aa994a2617e37d8fe4777ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2cc453bab04b5b001dd69bff7332c5be6f1c0a226acc67a7627af6982c686`

```dockerfile
```

-	Layers:
	-	`sha256:d3c75681fe65dbce30d8ec7dc2797a36440290e1eaf30506c2976d1affb63878`  
		Last Modified: Tue, 24 Sep 2024 01:00:54 GMT  
		Size: 11.3 KB (11283 bytes)  
		MIME: application/vnd.in-toto+json
