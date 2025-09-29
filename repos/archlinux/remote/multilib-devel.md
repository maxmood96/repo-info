## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:88376c49d29671bdda84f0274d874d2deb7680c921a67df881aa14bee3d1782d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f142967a07452f603ec8c06a0a5702998f8bb6625eaac2677715119caad20c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341155858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8290d444910aa65b516a9a665598535e1852c11a08c62630ed13b19e809e8bdb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.version=20250928.0.426921
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.created=2025-09-28T00:07:11+00:00
# Sun, 28 Sep 2025 00:07:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250928.0.426921' /etc/os-release # buildkit
# Sun, 28 Sep 2025 00:07:11 GMT
ENV LANG=C.UTF-8
# Sun, 28 Sep 2025 00:07:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:fa34bc9c8c7971a5a6d6ad411a4d1edfdaad82f213badb3427223ae31a0e7b62`  
		Last Modified: Mon, 29 Sep 2025 20:08:25 GMT  
		Size: 341.1 MB (341145597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce6e0fd4ce0734915d1c0c8164768fe5fc2751618ac97687d91ffdaba8c0c5c`  
		Last Modified: Mon, 29 Sep 2025 17:31:00 GMT  
		Size: 10.3 KB (10261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:e2af8f86891d8c7f2c6a5a752a66a179b7b89a6f7bc346456bbd81ddbe66fb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12398940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170d093347259d57127a005fda160e56160cc0ea051f623111657db7f1564bee`

```dockerfile
```

-	Layers:
	-	`sha256:dbc7e9706418e308a813fae0dba6bc723aef0f937175c5434a97a4967903519f`  
		Last Modified: Mon, 29 Sep 2025 19:48:30 GMT  
		Size: 12.4 MB (12387131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2063d1099c1fa1eecadebec0d0d996f748675dfda68332905d0b89ae8d98d6e0`  
		Last Modified: Mon, 29 Sep 2025 19:48:31 GMT  
		Size: 11.8 KB (11809 bytes)  
		MIME: application/vnd.in-toto+json
