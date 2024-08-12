## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:85386aeb0b8b40b2aa306056c1d9c8827356cfd9b5d74ae159092d46a0a6a4b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d703d0c3d9c2b43c45d685c61a630a3fb6b434bdaf92f4ff3b1fa6a19ce9fa38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271722146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bb71975f3172ab5edcfa81715b2583b3a3e6d7e029bcf509b8ac25b4c52832`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20240811.0.253648
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-08-11T00:07:52+00:00
# Sun, 11 Aug 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240811.0.253648' /etc/os-release # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 11 Aug 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8f5ad95fba3c70fdb088c4d4dece0a1ffccd67e67c78a7ea0c15051628382041`  
		Last Modified: Mon, 12 Aug 2024 16:57:04 GMT  
		Size: 271.7 MB (271713096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057791028ae05dcb6e7c4030c6492f3fc12a183a81f36a8c8b75e1bc3d69ced0`  
		Last Modified: Mon, 12 Aug 2024 16:57:00 GMT  
		Size: 9.1 KB (9050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2375f7922dfeca8b3d63beb27436f8bcdc3da08aa71b8c1db5651404f3dfd3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848ad116af6813b4c1dc71479281d8a646ced7992f6e1b114ca1f80ceb7f2bcd`

```dockerfile
```

-	Layers:
	-	`sha256:468170ebc267371f1741132b2b6d225e468cbfbf555cd0a68829fc806c7434ab`  
		Last Modified: Mon, 12 Aug 2024 16:57:00 GMT  
		Size: 11.8 MB (11818138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c668b256c4301ef947eb69ca00450c8fe9e2f8077d9f115078bcf9fd33e047`  
		Last Modified: Mon, 12 Aug 2024 16:57:00 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
