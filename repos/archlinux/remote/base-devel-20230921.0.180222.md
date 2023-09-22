## `archlinux:base-devel-20230921.0.180222`

```console
$ docker pull archlinux@sha256:bf5c44307643441db1a7646017c4f673476488a663e3ef196afcfdca20bd38b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230921.0.180222` - linux; amd64

```console
$ docker pull archlinux@sha256:781932307cf0d6ef99f92e03584498971d028cc0ec6828e77c6fd3a7dd819384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265829206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801b498cd83a43c68bf029d5a2fe6edacaf6c9ff9f75660f54e2c2dd9b823924`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.version=20230921.0.180222
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.revision=c432cbcbe27301dd9b2f4e1300b5ca0ff875e1ca
# Thu, 21 Sep 2023 23:21:05 GMT
LABEL org.opencontainers.image.created=2023-09-21T04:21:57+00:00
# Thu, 21 Sep 2023 23:21:17 GMT
COPY dir:54b78287ff1869fd2434a586fb08252b6683ddb826baafe37e7dbd6674f5626d in / 
# Thu, 21 Sep 2023 23:21:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230921.0.180222' /etc/os-release
# Thu, 21 Sep 2023 23:21:20 GMT
ENV LANG=C.UTF-8
# Thu, 21 Sep 2023 23:21:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:22c1a814f5a46ebf6beeb730dfd23c0c6ae36f4284c4c394f1aa3c9855f2c7ed`  
		Last Modified: Thu, 21 Sep 2023 23:22:43 GMT  
		Size: 265.8 MB (265820308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc5d45db49a8b45c72a8a11242628ec79b4b5045d1c07e5a958203ea6c4907a`  
		Last Modified: Thu, 21 Sep 2023 23:22:07 GMT  
		Size: 8.9 KB (8898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
