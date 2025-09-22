## `archlinux:latest`

```console
$ docker pull archlinux@sha256:2eb1a56a6036b1f70e63ca714814fe304a8f20d29ab425b4f056f34508500000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:16a95721ca6e63048ca1ca960b4ac8d9a5c74609d46954ef792a5e1360f41069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164710165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffd4a0cbb9673a6d6364ffef73b1627819f21c569710dadfa7a8a8273f35e52`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:178f25afaa61842b62d72a1943af8d3e78aee9a28649f53b0d2bdfce5c3620c4`  
		Last Modified: Mon, 22 Sep 2025 16:51:27 GMT  
		Size: 164.7 MB (164701824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc5f4896ee5f282a483cf3bdfa35a12103e2d5bc65dde7d05ba31808f47ca4`  
		Last Modified: Mon, 22 Sep 2025 16:51:13 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:41822909d08eb83c13857b357f83b78d0425370d34b34243713c362d5d2acce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0591214c03fac9c8bc073cf5d069f47bd2cf3dd0b7f8e615ea9a9508047d2240`

```dockerfile
```

-	Layers:
	-	`sha256:6697f22c06f0934acaef7765347f2a10a3072be97462c9990fc15769d9363182`  
		Last Modified: Mon, 22 Sep 2025 19:48:17 GMT  
		Size: 8.2 MB (8217061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c3ab3330f5682f771e21732c823f450549a383ab6c5dbb58934cc7278f014b`  
		Last Modified: Mon, 22 Sep 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
