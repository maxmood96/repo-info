## `archlinux:base-devel-20250928.0.426921`

```console
$ docker pull archlinux@sha256:5d95edcb6e10fd865e827e93749ecd425f5056880a5a1d8971f5f2a96c7b5a9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250928.0.426921` - linux; amd64

```console
$ docker pull archlinux@sha256:a76427cd2d3c2153fda2544bb988e9a5a0c6a7c9aeead8f50c437a5cfa3baecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289836820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca91498dc7c82e2e2d19d1a3cc97457d83aebe72b8b9af226adf0e24dca43c9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Sep 2025 00:07:11 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:00379b9bac0d799a3b12574884a943b938ea4344c8cc41124041c0afd05ac668`  
		Last Modified: Mon, 29 Sep 2025 19:50:37 GMT  
		Size: 289.8 MB (289827676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e52b0a8b4c1c01761221ef098a893bdd292b95f2a84faade66d02ac0c7302b`  
		Last Modified: Mon, 29 Sep 2025 17:31:05 GMT  
		Size: 9.1 KB (9144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250928.0.426921` - unknown; unknown

```console
$ docker pull archlinux@sha256:b449b544ff923113301c2eae816d55b18a395c5ff0e350a830ce079c6fe2c552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90ffebd7845e40d975f69d3b5a946f01bfc3325494150f11e559db34c852a5`

```dockerfile
```

-	Layers:
	-	`sha256:e5644a69415b56b12758dd7e5f1c317dc633928cf9c7cf44a92eac3e57691daa`  
		Last Modified: Mon, 29 Sep 2025 19:48:26 GMT  
		Size: 12.1 MB (12118343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87f634aae0d81b5b9221e128ad4529fdbec5325e74f7ff78036d2e2092a624e`  
		Last Modified: Mon, 29 Sep 2025 19:48:27 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
