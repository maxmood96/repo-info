## `archlinux:base-devel-20250629.0.373469`

```console
$ docker pull archlinux@sha256:16c85e56b0758a09815b39463a9bc2bbc870b2599c479ef947a2824281ca500c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250629.0.373469` - linux; amd64

```console
$ docker pull archlinux@sha256:f2d006725e76c1bda4bf675b9ae18013ef016436a803205c5ec12e9a7d7ce919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287795686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdd57aff9175c80d61aaf62d4c588048ad8037d5c602145b6f86760471a5a0c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250629.0.373469
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-06-29T00:07:42+00:00
# Sun, 29 Jun 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250629.0.373469' /etc/os-release # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 29 Jun 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ee5dff51893a25e6219969818aad60db02458d95032d1202c08ff1d96fb75630`  
		Last Modified: Mon, 30 Jun 2025 19:48:47 GMT  
		Size: 287.8 MB (287786527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e875a54ba2950610689aa075c30f55c0cfee42d2c2285e0d2ac120b9c9ed73`  
		Last Modified: Mon, 30 Jun 2025 17:17:34 GMT  
		Size: 9.2 KB (9159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250629.0.373469` - unknown; unknown

```console
$ docker pull archlinux@sha256:9291d40a1b644810c3990b1a2305d037476d02116cfa22e43441b1470ccc007c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12022005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb04097676ff2776f38fd790b4d73299958b3a88efda7ed604aa7ee2c7459d1c`

```dockerfile
```

-	Layers:
	-	`sha256:d06d076ded6a16ef432cd3a7f7705791aa26014f900544759263e4959f119939`  
		Last Modified: Mon, 30 Jun 2025 19:48:21 GMT  
		Size: 12.0 MB (12010251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f663588b265114c0fda38f02170232bbf8a6d44b0bb0156cfeff37d2e581d0`  
		Last Modified: Mon, 30 Jun 2025 19:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
