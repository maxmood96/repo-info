<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20231015.0.185077`](#archlinuxbase-202310150185077)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20231015.0.185077`](#archlinuxbase-devel-202310150185077)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:d5d55333006c8ff6191bc3bad3b16753b22f66e1e501fa2849f988689b89003d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:f481361e47643722d235d96d043832cdab142f0c417cd437235175c7cada11e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146951398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca64474746f3ede1e2e0b19f3c66ddbbd06d57b1b7a1af78f90dac4501eeb4b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.version=20231015.0.185077
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.revision=e688cede58b6771ce1117271551c1f0c57113614
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.created=2023-10-15T00:07:07+00:00
# Tue, 17 Oct 2023 00:22:42 GMT
COPY dir:b8b75ff42600e2b40c3daeb7fc9c7b2e47bfdc63d8e8d66708606c5d32c93947 in / 
# Tue, 17 Oct 2023 00:22:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231015.0.185077' /etc/os-release
# Tue, 17 Oct 2023 00:22:43 GMT
ENV LANG=C.UTF-8
# Tue, 17 Oct 2023 00:22:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e87e35f4229900ce11b8b5304ee4f9c403dd7e1e00086f97931aa738d7b9436e`  
		Last Modified: Tue, 17 Oct 2023 00:24:25 GMT  
		Size: 146.9 MB (146943263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187a484914fdf4c436a6170358e29bb55ade4e4fb3647a1b02ec1218a58562ef`  
		Last Modified: Tue, 17 Oct 2023 00:24:06 GMT  
		Size: 8.1 KB (8135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20231015.0.185077`

```console
$ docker pull archlinux@sha256:d5d55333006c8ff6191bc3bad3b16753b22f66e1e501fa2849f988689b89003d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20231015.0.185077` - linux; amd64

```console
$ docker pull archlinux@sha256:f481361e47643722d235d96d043832cdab142f0c417cd437235175c7cada11e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146951398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca64474746f3ede1e2e0b19f3c66ddbbd06d57b1b7a1af78f90dac4501eeb4b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.version=20231015.0.185077
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.revision=e688cede58b6771ce1117271551c1f0c57113614
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.created=2023-10-15T00:07:07+00:00
# Tue, 17 Oct 2023 00:22:42 GMT
COPY dir:b8b75ff42600e2b40c3daeb7fc9c7b2e47bfdc63d8e8d66708606c5d32c93947 in / 
# Tue, 17 Oct 2023 00:22:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231015.0.185077' /etc/os-release
# Tue, 17 Oct 2023 00:22:43 GMT
ENV LANG=C.UTF-8
# Tue, 17 Oct 2023 00:22:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e87e35f4229900ce11b8b5304ee4f9c403dd7e1e00086f97931aa738d7b9436e`  
		Last Modified: Tue, 17 Oct 2023 00:24:25 GMT  
		Size: 146.9 MB (146943263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187a484914fdf4c436a6170358e29bb55ade4e4fb3647a1b02ec1218a58562ef`  
		Last Modified: Tue, 17 Oct 2023 00:24:06 GMT  
		Size: 8.1 KB (8135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:7c4e1da516627362dfd40c9c13a073ebaffb5235b9850ebcd6deb508a9f25dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b10ae4fc21300a3fa02a38a555fec7caf5e6fdba9eb6c0dc4d9c9eed215635a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (264987172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700620546cefaa4299585f515370a74fe2703fdf7087a56ed5a0cddda2a1c0ac`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.version=20231015.0.185077
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.revision=e688cede58b6771ce1117271551c1f0c57113614
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.created=2023-10-15T00:07:15+00:00
# Tue, 17 Oct 2023 00:23:44 GMT
COPY dir:edc81e4213180b4af98cf7d3cdb95101b56d8b3847d7ed2f35c74dad3808c889 in / 
# Tue, 17 Oct 2023 00:23:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231015.0.185077' /etc/os-release
# Tue, 17 Oct 2023 00:23:47 GMT
ENV LANG=C.UTF-8
# Tue, 17 Oct 2023 00:23:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cba449e246f567dae7b0628945c680e924813660f6110cd2760cdd4cfb76a353`  
		Last Modified: Tue, 17 Oct 2023 00:25:14 GMT  
		Size: 265.0 MB (264978249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159d2f97894c6a8e686f9e98c78575b91a09a9c314d152ed68df0a4db2717d7`  
		Last Modified: Tue, 17 Oct 2023 00:24:38 GMT  
		Size: 8.9 KB (8923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20231015.0.185077`

```console
$ docker pull archlinux@sha256:7c4e1da516627362dfd40c9c13a073ebaffb5235b9850ebcd6deb508a9f25dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20231015.0.185077` - linux; amd64

```console
$ docker pull archlinux@sha256:b10ae4fc21300a3fa02a38a555fec7caf5e6fdba9eb6c0dc4d9c9eed215635a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (264987172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700620546cefaa4299585f515370a74fe2703fdf7087a56ed5a0cddda2a1c0ac`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.version=20231015.0.185077
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.revision=e688cede58b6771ce1117271551c1f0c57113614
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.created=2023-10-15T00:07:15+00:00
# Tue, 17 Oct 2023 00:23:44 GMT
COPY dir:edc81e4213180b4af98cf7d3cdb95101b56d8b3847d7ed2f35c74dad3808c889 in / 
# Tue, 17 Oct 2023 00:23:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231015.0.185077' /etc/os-release
# Tue, 17 Oct 2023 00:23:47 GMT
ENV LANG=C.UTF-8
# Tue, 17 Oct 2023 00:23:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cba449e246f567dae7b0628945c680e924813660f6110cd2760cdd4cfb76a353`  
		Last Modified: Tue, 17 Oct 2023 00:25:14 GMT  
		Size: 265.0 MB (264978249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159d2f97894c6a8e686f9e98c78575b91a09a9c314d152ed68df0a4db2717d7`  
		Last Modified: Tue, 17 Oct 2023 00:24:38 GMT  
		Size: 8.9 KB (8923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:d5d55333006c8ff6191bc3bad3b16753b22f66e1e501fa2849f988689b89003d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:f481361e47643722d235d96d043832cdab142f0c417cd437235175c7cada11e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146951398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca64474746f3ede1e2e0b19f3c66ddbbd06d57b1b7a1af78f90dac4501eeb4b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.version=20231015.0.185077
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.revision=e688cede58b6771ce1117271551c1f0c57113614
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.created=2023-10-15T00:07:07+00:00
# Tue, 17 Oct 2023 00:22:42 GMT
COPY dir:b8b75ff42600e2b40c3daeb7fc9c7b2e47bfdc63d8e8d66708606c5d32c93947 in / 
# Tue, 17 Oct 2023 00:22:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231015.0.185077' /etc/os-release
# Tue, 17 Oct 2023 00:22:43 GMT
ENV LANG=C.UTF-8
# Tue, 17 Oct 2023 00:22:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e87e35f4229900ce11b8b5304ee4f9c403dd7e1e00086f97931aa738d7b9436e`  
		Last Modified: Tue, 17 Oct 2023 00:24:25 GMT  
		Size: 146.9 MB (146943263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187a484914fdf4c436a6170358e29bb55ade4e4fb3647a1b02ec1218a58562ef`  
		Last Modified: Tue, 17 Oct 2023 00:24:06 GMT  
		Size: 8.1 KB (8135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
