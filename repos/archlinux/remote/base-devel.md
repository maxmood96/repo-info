## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:f44a86aa1626ff15535a1f442f73c84e3319b6e420e6176118ad11f7e401378a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6413de4bb40c6c97e123f5e891790fe00997cd7c23167d43f80c9a5d3881a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287033912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a5211731e9cba4e31d1832e7d36d31927738b6895fa14440fe6d7cf8d053bc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:19e3d5faef4b620e1ec0e4b4de82122aae646a54d343f04ad69171021e3b66b2`  
		Last Modified: Mon, 19 May 2025 23:02:09 GMT  
		Size: 287.0 MB (287024711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad70d5d372d9f7670b6c2fba64439a2e2f61a07a7d6e7ad4cac20ffd1317f7`  
		Last Modified: Mon, 19 May 2025 23:02:03 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c4a1f95d9c45869f5338ae8558ec11b12af727a5bcd8074c46fb82d4beb62cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12041406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb95f4b99020eccdbb70256c6d0462c1559824987c699d3e3840e7d85b24e7b7`

```dockerfile
```

-	Layers:
	-	`sha256:f933c4c9dbbb10d2a33ebfcc6a4fff177ab27e31fbed3a233e42be180f15db28`  
		Last Modified: Mon, 19 May 2025 23:02:04 GMT  
		Size: 12.0 MB (12029652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43f79935b373bbc3e71f16fc18782ca266826631d0f926e8db844f369fc0924`  
		Last Modified: Mon, 19 May 2025 23:02:03 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
