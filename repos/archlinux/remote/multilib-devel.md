## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:787247c74479f2dadbd1a1a336e0c26d8312d54f884afc67b29bba5bde56e995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:16d590427240779ff96610a996f2acc10041ee17d59c90dab981257e47bd0aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321627592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cce18feb462cc0ce674952344569566b6d3b781192af2dede313cbb971424f9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b39c3f3d5831908f56eae8d8bceedb49c7424402515d9cf9b1feb3ba6c022781`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 321.6 MB (321617407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34176b4a87a58fee083b819f8974173ec092d49362333ea31c72a416a8627019`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 10.2 KB (10185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:b00b1a08a255a55cefb94284cfddd986f1d06d995c83a826c7aa3aeea42ac9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b3d81cb60807ca62152dc5bc418444bc5920f97fd9b43f54787f51762401a5`

```dockerfile
```

-	Layers:
	-	`sha256:84e929d0df5ed6d0a81c6ddd964836dcf541ba6592fe33e93831a489960b988d`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 12.1 MB (12085490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056aa45e388121c0566282711b40861fe85dfd388a0eb377497b49857547d658`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
