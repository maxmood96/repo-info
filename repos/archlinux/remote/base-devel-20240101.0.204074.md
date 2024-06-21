## `archlinux:base-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:4d4821711ba77904458da94ad3db7de44184c6945eb684f96438fe7778b2420f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:c65736805583204ee36b28b34aa7106df9e45b35ae545a53ebe5b771171a3e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172c561b410c36e9c5d15433c5f5b359492bffd07b3156ea99b13a0ed08e8519`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad59c724b2d7e7041a88eae078be10f472732091bab7b3ff59e2bbd5056e65f6`  
		Last Modified: Wed, 29 May 2024 19:57:22 GMT  
		Size: 266.2 MB (266230027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdeb6c4b76bd400e6456522b9754397780a2bd2609e44734011239bb5b12f0e`  
		Last Modified: Thu, 20 Jun 2024 20:55:35 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240101.0.204074` - unknown; unknown

```console
$ docker pull archlinux@sha256:03ea318b897f20062c906641fee669eafa6b82b12156a6e81e1bc1d98a82aa74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11620644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428ac9355b664ed047a7eb9b6f0d8fc1dacbb8920578be8a8cd377e9d4e3f273`

```dockerfile
```

-	Layers:
	-	`sha256:c6bfffb25a24756dd9a6b4415f9a6ebed5af1f320f13f220ddb9a139aa52fc89`  
		Last Modified: Thu, 20 Jun 2024 20:55:35 GMT  
		Size: 11.6 MB (11609141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d7f8265cb5ae91996336b2febf54bda9ca777299dcabf5e0bee41f2d995651`  
		Last Modified: Thu, 20 Jun 2024 20:55:34 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
