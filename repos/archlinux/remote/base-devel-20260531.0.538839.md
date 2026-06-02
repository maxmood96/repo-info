## `archlinux:base-devel-20260531.0.538839`

```console
$ docker pull archlinux@sha256:c84ad63503efc5d386e30a5f44945fa8eee10fcb21b3d5fceda260783de394ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260531.0.538839` - linux; amd64

```console
$ docker pull archlinux@sha256:b020e4b83a278d78028c89186b7f937a92e57a59d800587b713af7f9bfc0d45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304004094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a65e6928d31336af0d1c66eae039c6bb18d2ab7872b527495aa306a5121de`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.version=20260531.0.538839
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 01 Jun 2026 21:31:03 GMT
LABEL org.opencontainers.image.created=2026-05-31T00:09:15+00:00
# Mon, 01 Jun 2026 21:31:03 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jun 2026 21:31:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260531.0.538839' /etc/os-release # buildkit
# Mon, 01 Jun 2026 21:31:16 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jun 2026 21:31:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9f04e3f1a44c3fcba4c558a3b057780df3a688b4965c0d7268b6118b903351f`  
		Last Modified: Mon, 01 Jun 2026 21:32:08 GMT  
		Size: 304.0 MB (303992683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5afeb8ece19bbc8a93dc14d6de8929c291eac60f32b49067e9806c8abf253c`  
		Last Modified: Mon, 01 Jun 2026 21:32:00 GMT  
		Size: 11.4 KB (11411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260531.0.538839` - unknown; unknown

```console
$ docker pull archlinux@sha256:15ea0abd8e9b686b416de361fc609d3ad69a6501dc5d103bccb61b311dee2df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14396300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7d33c344487675eef6e28c739bb29f0dd4ee66301a800c6be9ae9e90e93517`

```dockerfile
```

-	Layers:
	-	`sha256:9074331b3600b9122731310f1090ebdfbef5b80ba81c3c69d455561c7325a10d`  
		Last Modified: Mon, 01 Jun 2026 21:32:01 GMT  
		Size: 14.4 MB (14384588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ad73ec17231b9ea1f9aa8ab786c5b63aa92b632e23a4680da5f40cedbbf4487`  
		Last Modified: Mon, 01 Jun 2026 21:32:00 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json
