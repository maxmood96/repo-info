<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241027.0.273886`](#archlinuxbase-202410270273886)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241027.0.273886`](#archlinuxbase-devel-202410270273886)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241027.0.273886`](#archlinuxmultilib-devel-202410270273886)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:65b8373574abc1afda6c77ca01bba81ba02cb3779ced8ae1b5cd29f48d75c4f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c9b9e00238d67eb25868d59c658b0566d49df3d0d5e6cfdc88a8099d966dfadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151211271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0783ec4488140fe48524781040a1528f957e86bd29f08e7fac97c155afdef7d6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a177a8b9b0eb48ecc5621b8999f2a3ffb3b838af7149516ae728e3de3d265c95`  
		Last Modified: Mon, 28 Oct 2024 17:57:21 GMT  
		Size: 151.2 MB (151202982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a98e2032b813b85b356987b3e9942c397d04b3452d988da53048eeaa9ef3ac3`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 8.3 KB (8289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:b5ac2147e2399d71365a4e21c3c04d34ff173a61be6b4756753b5b2ff52b429c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dad605717143b6aa0b156ac2b8dd89c837af0aa477b8f57bfa5dd9d2f4c6cf4`

```dockerfile
```

-	Layers:
	-	`sha256:c501b60485132b041b536e0c71104a796f62edb28dcdd20446461663d50fb590`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 8.1 MB (8144185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d231dd67e2a4baa5f9582e3adacde08c6f019ea6c1221160eec75e5304154f`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241027.0.273886`

```console
$ docker pull archlinux@sha256:65b8373574abc1afda6c77ca01bba81ba02cb3779ced8ae1b5cd29f48d75c4f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20241027.0.273886` - linux; amd64

```console
$ docker pull archlinux@sha256:c9b9e00238d67eb25868d59c658b0566d49df3d0d5e6cfdc88a8099d966dfadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151211271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0783ec4488140fe48524781040a1528f957e86bd29f08e7fac97c155afdef7d6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a177a8b9b0eb48ecc5621b8999f2a3ffb3b838af7149516ae728e3de3d265c95`  
		Last Modified: Mon, 28 Oct 2024 17:57:21 GMT  
		Size: 151.2 MB (151202982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a98e2032b813b85b356987b3e9942c397d04b3452d988da53048eeaa9ef3ac3`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 8.3 KB (8289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20241027.0.273886` - unknown; unknown

```console
$ docker pull archlinux@sha256:b5ac2147e2399d71365a4e21c3c04d34ff173a61be6b4756753b5b2ff52b429c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dad605717143b6aa0b156ac2b8dd89c837af0aa477b8f57bfa5dd9d2f4c6cf4`

```dockerfile
```

-	Layers:
	-	`sha256:c501b60485132b041b536e0c71104a796f62edb28dcdd20446461663d50fb590`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 8.1 MB (8144185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d231dd67e2a4baa5f9582e3adacde08c6f019ea6c1221160eec75e5304154f`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:d1182fe9683fd80afac359754f606aa1fbb74aa2e6f65a9395be83a95bb8f953
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:39908e5005aa727e93e36fa4b741a1ed22fd7b2db83e264ce0acdc7aea334397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272205935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b21ceeb73c50dc0b884143ea2feed0a0b9c919cfa42b8f38336d80a4c7ffa7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:02a5a1341bbcd83e0148b5fd871fbadb41badae053e4d579e9fc6fe7b740ea1b`  
		Last Modified: Mon, 28 Oct 2024 17:58:12 GMT  
		Size: 272.2 MB (272196934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de547d0c8aa87918635917dd8ca511ca2788075fa3529c53b174d64c69ecae21`  
		Last Modified: Mon, 28 Oct 2024 17:58:03 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8efad37ba464c1863be291efef4ece9e74041c53fc6b6f4b24f8bcabeba05357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11962175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aadfeb0ee6b15d9c7c106617a93fe593349825f5112c9145c345a6b030794d`

```dockerfile
```

-	Layers:
	-	`sha256:de5c521344689eb688ae68a376b9bdcc5a4d4375089c843e5e108f47bb390cdb`  
		Last Modified: Mon, 28 Oct 2024 17:58:04 GMT  
		Size: 12.0 MB (11950638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add305c0d4ca9e7110af0d941275e8ed60f89ca5bd83f12865dd009a49d5da6f`  
		Last Modified: Mon, 28 Oct 2024 17:58:03 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241027.0.273886`

```console
$ docker pull archlinux@sha256:d1182fe9683fd80afac359754f606aa1fbb74aa2e6f65a9395be83a95bb8f953
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241027.0.273886` - linux; amd64

```console
$ docker pull archlinux@sha256:39908e5005aa727e93e36fa4b741a1ed22fd7b2db83e264ce0acdc7aea334397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272205935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b21ceeb73c50dc0b884143ea2feed0a0b9c919cfa42b8f38336d80a4c7ffa7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:02a5a1341bbcd83e0148b5fd871fbadb41badae053e4d579e9fc6fe7b740ea1b`  
		Last Modified: Mon, 28 Oct 2024 17:58:12 GMT  
		Size: 272.2 MB (272196934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de547d0c8aa87918635917dd8ca511ca2788075fa3529c53b174d64c69ecae21`  
		Last Modified: Mon, 28 Oct 2024 17:58:03 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241027.0.273886` - unknown; unknown

```console
$ docker pull archlinux@sha256:8efad37ba464c1863be291efef4ece9e74041c53fc6b6f4b24f8bcabeba05357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11962175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aadfeb0ee6b15d9c7c106617a93fe593349825f5112c9145c345a6b030794d`

```dockerfile
```

-	Layers:
	-	`sha256:de5c521344689eb688ae68a376b9bdcc5a4d4375089c843e5e108f47bb390cdb`  
		Last Modified: Mon, 28 Oct 2024 17:58:04 GMT  
		Size: 12.0 MB (11950638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add305c0d4ca9e7110af0d941275e8ed60f89ca5bd83f12865dd009a49d5da6f`  
		Last Modified: Mon, 28 Oct 2024 17:58:03 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:65b8373574abc1afda6c77ca01bba81ba02cb3779ced8ae1b5cd29f48d75c4f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c9b9e00238d67eb25868d59c658b0566d49df3d0d5e6cfdc88a8099d966dfadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151211271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0783ec4488140fe48524781040a1528f957e86bd29f08e7fac97c155afdef7d6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a177a8b9b0eb48ecc5621b8999f2a3ffb3b838af7149516ae728e3de3d265c95`  
		Last Modified: Mon, 28 Oct 2024 17:57:21 GMT  
		Size: 151.2 MB (151202982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a98e2032b813b85b356987b3e9942c397d04b3452d988da53048eeaa9ef3ac3`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 8.3 KB (8289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:b5ac2147e2399d71365a4e21c3c04d34ff173a61be6b4756753b5b2ff52b429c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dad605717143b6aa0b156ac2b8dd89c837af0aa477b8f57bfa5dd9d2f4c6cf4`

```dockerfile
```

-	Layers:
	-	`sha256:c501b60485132b041b536e0c71104a796f62edb28dcdd20446461663d50fb590`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 8.1 MB (8144185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d231dd67e2a4baa5f9582e3adacde08c6f019ea6c1221160eec75e5304154f`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:996271fe443a25059a31bae6863db63df6e090d8e81d4cdda7bb6a214c3d64ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d33a25b63b044fe7db4b635f8b8e269f0f61d1b8012185ce8e2312b2a1d67bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322055353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c538f252b2b78620cb60b4de1f422977526c2b9f2b6686b47d8bdec4e3fc9c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:826dcc06a75ff2538ee33ec9ad2888004cf6fbedaa6be4d815b2860824d9f2b4`  
		Last Modified: Mon, 28 Oct 2024 17:58:05 GMT  
		Size: 322.0 MB (322045198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8b3e30305e384e9de73f35d0185bcd40fbe39574152d686d8b39a00169e5c6`  
		Last Modified: Mon, 28 Oct 2024 17:57:59 GMT  
		Size: 10.2 KB (10155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:76d67f961cd5fe6d3ace9d34b7169bc44374801a7778595fdd5db6da21ea590e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12231028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21456cda2ce4b72ae58b39460c8becde13cd7c8dd421a8bd40ccf997847f95bf`

```dockerfile
```

-	Layers:
	-	`sha256:f233fe4a18354999f5a6e562c448bdc7a4e133c18a39830a0c89a042b77bd557`  
		Last Modified: Mon, 28 Oct 2024 17:58:00 GMT  
		Size: 12.2 MB (12219434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f334fa056038032813133136ccb698bcf7a0f27e0094116df1ae0c1470201b`  
		Last Modified: Mon, 28 Oct 2024 17:57:59 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241027.0.273886`

```console
$ docker pull archlinux@sha256:996271fe443a25059a31bae6863db63df6e090d8e81d4cdda7bb6a214c3d64ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241027.0.273886` - linux; amd64

```console
$ docker pull archlinux@sha256:d33a25b63b044fe7db4b635f8b8e269f0f61d1b8012185ce8e2312b2a1d67bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322055353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c538f252b2b78620cb60b4de1f422977526c2b9f2b6686b47d8bdec4e3fc9c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:826dcc06a75ff2538ee33ec9ad2888004cf6fbedaa6be4d815b2860824d9f2b4`  
		Last Modified: Mon, 28 Oct 2024 17:58:05 GMT  
		Size: 322.0 MB (322045198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8b3e30305e384e9de73f35d0185bcd40fbe39574152d686d8b39a00169e5c6`  
		Last Modified: Mon, 28 Oct 2024 17:57:59 GMT  
		Size: 10.2 KB (10155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241027.0.273886` - unknown; unknown

```console
$ docker pull archlinux@sha256:76d67f961cd5fe6d3ace9d34b7169bc44374801a7778595fdd5db6da21ea590e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12231028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21456cda2ce4b72ae58b39460c8becde13cd7c8dd421a8bd40ccf997847f95bf`

```dockerfile
```

-	Layers:
	-	`sha256:f233fe4a18354999f5a6e562c448bdc7a4e133c18a39830a0c89a042b77bd557`  
		Last Modified: Mon, 28 Oct 2024 17:58:00 GMT  
		Size: 12.2 MB (12219434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f334fa056038032813133136ccb698bcf7a0f27e0094116df1ae0c1470201b`  
		Last Modified: Mon, 28 Oct 2024 17:57:59 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json
