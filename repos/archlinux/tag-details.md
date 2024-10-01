<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240929.0.266368`](#archlinuxbase-202409290266368)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240929.0.266368`](#archlinuxbase-devel-202409290266368)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240929.0.266368`](#archlinuxmultilib-devel-202409290266368)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:c8501ab8b970205491501ba01d9bce9a04d70537fc15596360f1ce1011b08569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a45700aba9079ee52d41d080d1aed39066e0867aa9beebcc695cd111c21964e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151190914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94a7c8f8266f9cdbd578e1d5fb550dd9f2311b523b23c648418db6356490234`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:7ddbe2be8d389ca48dffe33e9c2cc9cc42a697902051e41777c3f38d5d133529`  
		Last Modified: Mon, 30 Sep 2024 23:11:22 GMT  
		Size: 151.2 MB (151182688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37561576c475eac7174073f448cc4d7cb50010a8824c054d93b01d3405485cc`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 8.2 KB (8226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:695ef93d80927410e8e69ecc29b51d94ef292b2ecb33bdc992a1e7ac8f8ec76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe361d1914f43ddd2e074e8ee3108ae79f040e50dff66ad09105afe9a122995`

```dockerfile
```

-	Layers:
	-	`sha256:fa44779a3be51b65fa3d5501ca4f91aa2096b037ec0f2f5893afdc1144496195`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 8.1 MB (8102285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40dd1c955fb739aa9dfb1b8ea50a71e4e1e088472d8543c9d9fea18a0ec26a1`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240929.0.266368`

```console
$ docker pull archlinux@sha256:c8501ab8b970205491501ba01d9bce9a04d70537fc15596360f1ce1011b08569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20240929.0.266368` - linux; amd64

```console
$ docker pull archlinux@sha256:a45700aba9079ee52d41d080d1aed39066e0867aa9beebcc695cd111c21964e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151190914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94a7c8f8266f9cdbd578e1d5fb550dd9f2311b523b23c648418db6356490234`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:7ddbe2be8d389ca48dffe33e9c2cc9cc42a697902051e41777c3f38d5d133529`  
		Last Modified: Mon, 30 Sep 2024 23:11:22 GMT  
		Size: 151.2 MB (151182688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37561576c475eac7174073f448cc4d7cb50010a8824c054d93b01d3405485cc`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 8.2 KB (8226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20240929.0.266368` - unknown; unknown

```console
$ docker pull archlinux@sha256:695ef93d80927410e8e69ecc29b51d94ef292b2ecb33bdc992a1e7ac8f8ec76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe361d1914f43ddd2e074e8ee3108ae79f040e50dff66ad09105afe9a122995`

```dockerfile
```

-	Layers:
	-	`sha256:fa44779a3be51b65fa3d5501ca4f91aa2096b037ec0f2f5893afdc1144496195`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 8.1 MB (8102285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40dd1c955fb739aa9dfb1b8ea50a71e4e1e088472d8543c9d9fea18a0ec26a1`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:5aecf156784feca2c4d42bc32a1dfb5634c49c4791756d2f59187d6af32cd716
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

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

### `archlinux:base-devel` - unknown; unknown

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

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:c8501ab8b970205491501ba01d9bce9a04d70537fc15596360f1ce1011b08569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:a45700aba9079ee52d41d080d1aed39066e0867aa9beebcc695cd111c21964e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151190914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94a7c8f8266f9cdbd578e1d5fb550dd9f2311b523b23c648418db6356490234`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:7ddbe2be8d389ca48dffe33e9c2cc9cc42a697902051e41777c3f38d5d133529`  
		Last Modified: Mon, 30 Sep 2024 23:11:22 GMT  
		Size: 151.2 MB (151182688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37561576c475eac7174073f448cc4d7cb50010a8824c054d93b01d3405485cc`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 8.2 KB (8226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:695ef93d80927410e8e69ecc29b51d94ef292b2ecb33bdc992a1e7ac8f8ec76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe361d1914f43ddd2e074e8ee3108ae79f040e50dff66ad09105afe9a122995`

```dockerfile
```

-	Layers:
	-	`sha256:fa44779a3be51b65fa3d5501ca4f91aa2096b037ec0f2f5893afdc1144496195`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 8.1 MB (8102285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40dd1c955fb739aa9dfb1b8ea50a71e4e1e088472d8543c9d9fea18a0ec26a1`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:071b4cb1f6db1871a75b5fa13e367fa0675d3a7b89837dec8b7086a70f8829ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:70645f647cd08d3f382fed4b38571c2aad78aeb575dd62a3c85abcf89e78d656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322031945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a43d2c52fc6c00026b3be459daf52b663135439774983ce94ea5d03fe127cfd`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
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
	-	`sha256:d7b7f73b0b674cd33738487d735a88a1d8e00ae4f0a094aa513f8841d187c55d`  
		Last Modified: Mon, 30 Sep 2024 23:12:17 GMT  
		Size: 322.0 MB (322021855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0436639ec6db38a92616a17c93af27037cfc1b1e5439f061ed2bf66161797f`  
		Last Modified: Mon, 30 Sep 2024 23:12:09 GMT  
		Size: 10.1 KB (10090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2d6fc250a4dc13839a029d53734a2b6fd2041b17a52cf948aed6378e7fef8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481d3ea760c1c4039e2b13c9ef290dfee13a7c3537b417aa850cbabbd8550a24`

```dockerfile
```

-	Layers:
	-	`sha256:757b9f215d8266fb6faa6938ae99995cfbcf36cf10eb9eb0b1f6cfc213b16fed`  
		Last Modified: Mon, 30 Sep 2024 23:12:10 GMT  
		Size: 12.2 MB (12167888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada334a1431c7dfb2e1c1fbb2e3e604d39d70cf1e7e458021b3f43d9dfc4ec49`  
		Last Modified: Mon, 30 Sep 2024 23:12:09 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240929.0.266368`

```console
$ docker pull archlinux@sha256:071b4cb1f6db1871a75b5fa13e367fa0675d3a7b89837dec8b7086a70f8829ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240929.0.266368` - linux; amd64

```console
$ docker pull archlinux@sha256:70645f647cd08d3f382fed4b38571c2aad78aeb575dd62a3c85abcf89e78d656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322031945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a43d2c52fc6c00026b3be459daf52b663135439774983ce94ea5d03fe127cfd`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
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
	-	`sha256:d7b7f73b0b674cd33738487d735a88a1d8e00ae4f0a094aa513f8841d187c55d`  
		Last Modified: Mon, 30 Sep 2024 23:12:17 GMT  
		Size: 322.0 MB (322021855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0436639ec6db38a92616a17c93af27037cfc1b1e5439f061ed2bf66161797f`  
		Last Modified: Mon, 30 Sep 2024 23:12:09 GMT  
		Size: 10.1 KB (10090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240929.0.266368` - unknown; unknown

```console
$ docker pull archlinux@sha256:2d6fc250a4dc13839a029d53734a2b6fd2041b17a52cf948aed6378e7fef8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481d3ea760c1c4039e2b13c9ef290dfee13a7c3537b417aa850cbabbd8550a24`

```dockerfile
```

-	Layers:
	-	`sha256:757b9f215d8266fb6faa6938ae99995cfbcf36cf10eb9eb0b1f6cfc213b16fed`  
		Last Modified: Mon, 30 Sep 2024 23:12:10 GMT  
		Size: 12.2 MB (12167888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada334a1431c7dfb2e1c1fbb2e3e604d39d70cf1e7e458021b3f43d9dfc4ec49`  
		Last Modified: Mon, 30 Sep 2024 23:12:09 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
