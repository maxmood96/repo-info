## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:8e9a67199c0e19b948e1fb2689e776badb2c809e60e245ec99f0c9fead3cdb89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b2b8809c3dd1a2615c0118e6fe14960e0f9e023bd93b2c4f27169d7fece6b134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280688675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a18fa20214e02eace3b3f6e7fab707d5e08a5975ee115c23eb441d0236d3db5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6ea895d481edad2d574c0da7ae67ab023c372f3339d132fbe9df2ed192e9af8c`  
		Last Modified: Mon, 17 Mar 2025 17:50:50 GMT  
		Size: 280.7 MB (280679605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e194902f33b02486da39c81de7fbff4e31abf37d09058562602565ec19de9e0b`  
		Last Modified: Mon, 17 Mar 2025 17:50:43 GMT  
		Size: 9.1 KB (9070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:28684ba8b71805f55134c30a43c7fd83dcbf78d57f68329d1138907e435d0ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11987671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652c325c88ad42fe1d579457298a9eaae37a062cb41a9135d8d4a9d2ce6622d8`

```dockerfile
```

-	Layers:
	-	`sha256:5b563dde661c80c1ba775a97b79912c37f36b0a916310b0313bcac0d51f5f793`  
		Last Modified: Mon, 17 Mar 2025 17:50:44 GMT  
		Size: 12.0 MB (11975917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1611911bbfe2fcd98c219696c4bf43e693d63ebf63476918626714f6535c797`  
		Last Modified: Mon, 17 Mar 2025 17:50:43 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
