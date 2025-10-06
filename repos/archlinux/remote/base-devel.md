## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b3809917ab5a7840d42237f5f92d92660cd036bd75ae343e7825e6a24401f166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:2f0f0994fcffdfa3d183aeb3ba6190bb67d4d180987ff566673173ee4f926378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290344795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5444ec66413f3126eab60368d32a466728c59ca1297eaea3ded36afc9608a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:31bd40284997e57aafb1578009aa7ac3eb161d57ef18a8620487b68765949955`  
		Last Modified: Mon, 06 Oct 2025 19:48:54 GMT  
		Size: 290.3 MB (290335625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0b90acc81c520a9d4565ebfecb4782cf769176ff2c131f34140f98407cca7`  
		Last Modified: Mon, 06 Oct 2025 17:56:13 GMT  
		Size: 9.2 KB (9170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:fdc3321b047599f5e4255ac1a5f549c462dd47466e1cf20b9a5a4a4bed8774ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12131338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbc7d5218e69dba0997074cae341e477f2cb05a570d0b3f8c3dea98accdc63d`

```dockerfile
```

-	Layers:
	-	`sha256:7763996dbe32382a63a8c5b101ac4fa133c1de8a74367c81428224b0c7838142`  
		Last Modified: Mon, 06 Oct 2025 19:48:31 GMT  
		Size: 12.1 MB (12119584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e7ccd02f79cae45ada89ad2554c01a9d5f597a7c8fe03da86013e13ec4c689`  
		Last Modified: Mon, 06 Oct 2025 19:48:32 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
