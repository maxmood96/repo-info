## `archlinux:base-devel-20251214.0.467559`

```console
$ docker pull archlinux@sha256:1635f3838c665558a2aaac32929470ef844f65be4acd5c47167c6d98d74baba2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251214.0.467559` - linux; amd64

```console
$ docker pull archlinux@sha256:3933d17afd7338682a5c67314e8cf4ba91a48d184264899b25e60ed4d8e68fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f17cb5ace583a497da558773ee52a532df623ede60a1a4308f51751649c7df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:32:17 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:32:24 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:32:24 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:32:24 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:28f03c6e8bb3a7030933065fad15d28b50b0bfc498ea6d4cedd92904feb81e22`  
		Last Modified: Mon, 15 Dec 2025 18:33:53 GMT  
		Size: 292.1 MB (292061547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e72afe4396e320604700a6d169207768e63d8b10b9db29238ad97c87ba906d4`  
		Last Modified: Mon, 15 Dec 2025 18:33:31 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251214.0.467559` - unknown; unknown

```console
$ docker pull archlinux@sha256:fc6186dd7214c50da7f91d520c46a383c3afa34531378ed11196ad1fe36478b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12142872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bda182f627f017a73b44b44a745ee4dc6df88ef22da981674c66fe9d804eed`

```dockerfile
```

-	Layers:
	-	`sha256:8d4a87d4642d8c4bafe737c0bed5c913d0f6ffd5e158140c2ed521500c86590d`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 12.1 MB (12131161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe7dc55e0051978bd4d4d28c0ce9d9eb840053e74da2febbba86a1c62e64ce5`  
		Last Modified: Mon, 15 Dec 2025 20:48:24 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
