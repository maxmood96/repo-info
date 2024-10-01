## `archlinux:base-devel-20240929.0.266368`

```console
$ docker pull archlinux@sha256:5aecf156784feca2c4d42bc32a1dfb5634c49c4791756d2f59187d6af32cd716
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240929.0.266368` - linux; amd64

```console
$ docker pull archlinux@sha256:ee95ae79c578a505e644cc2f67b13fcf449fafcad7274ca9cf0f9f1bcff0adeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272191352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03fad26dddebd305d273d74005fbcf9024b42a644755a65058bbc634ab26774`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.version=20240929.0.266368
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.created=2024-09-29T00:07:44+00:00
# Sun, 29 Sep 2024 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Sep 2024 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240929.0.266368' /etc/os-release # buildkit
# Sun, 29 Sep 2024 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 29 Sep 2024 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35e5b5b79eb04f372a7687fbd798cecf1b3ee200cdcf47f5a381487db935df07`  
		Last Modified: Mon, 30 Sep 2024 23:11:52 GMT  
		Size: 272.2 MB (272182325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adbf413c5226270f7c0ccf3d26804c50371247a9716aa89d9b507b661427f27`  
		Last Modified: Mon, 30 Sep 2024 23:11:49 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240929.0.266368` - unknown; unknown

```console
$ docker pull archlinux@sha256:fc40a9fae8c3baead830642e072c9ffb9d8e020f1b54ae39d7ff69496ee232c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11912079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575e574f6276689e8b67a65cca3fdcd157722fe24c113c42200b531b7088e85e`

```dockerfile
```

-	Layers:
	-	`sha256:03eb1a3ddf841c99a9b0d0d0f99caeef7ad69f63ee56f6a3b4d2b97abbd085c7`  
		Last Modified: Mon, 30 Sep 2024 23:11:49 GMT  
		Size: 11.9 MB (11900576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90dca0a04a7aeb2739d38b87fd75bc52c999eedba96ec23740f866dd2f136e13`  
		Last Modified: Mon, 30 Sep 2024 23:11:49 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
