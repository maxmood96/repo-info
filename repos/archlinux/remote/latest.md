## `archlinux:latest`

```console
$ docker pull archlinux@sha256:97c56e9c792dc50df96c77187255a752f479698c9beb4aa9caeb9fe4639a7590
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0ae99d31dec8d486b79831481e66be38eb384e5ae27c28929a9da1a03dbe535e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164063896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d908c4dc4a4535c266e1a68debfc16b80e51cd3582876df48bc443dd09618d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f6dbfeb25e4d5cd2e7c173987dcb74e3620311b54f906cbddb04b52d6ef1fff`  
		Last Modified: Mon, 25 Aug 2025 22:48:33 GMT  
		Size: 164.1 MB (164055570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e4b51ca8e610cc6392506347415c55a2a2491d5d2d5166d494bde2d459548`  
		Last Modified: Mon, 25 Aug 2025 19:55:33 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:6fa71df4c776e0ef083323e58dc17905f9c1bcfcab40d241f109a148b865341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d8418d52c7ab1737ef1d0d0f5f40e684104bf1dfa19efb1f9f0ed23eeda41d`

```dockerfile
```

-	Layers:
	-	`sha256:62f615734ad75439f23f74085d2e67a7570affe1a9186fb0e57a2e3027ea5530`  
		Last Modified: Mon, 25 Aug 2025 22:48:18 GMT  
		Size: 8.2 MB (8162397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9ed6f343a725a9e636432546601265ceb6d4cc9c3ae6e9f29a0d8c580717da`  
		Last Modified: Mon, 25 Aug 2025 22:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
