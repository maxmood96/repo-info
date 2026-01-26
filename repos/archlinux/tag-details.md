<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260125.0.484595`](#archlinuxbase-202601250484595)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260125.0.484595`](#archlinuxbase-devel-202601250484595)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260125.0.484595`](#archlinuxmultilib-devel-202601250484595)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:3706b9784abbea6c3cae6da206b0f3fb3b7d363408db591604578bc32e022359
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:e4ed0eedd03eae66b22fed7ed701bf2f613006ba53f17cbd7052210b0266eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f60429ea8275a3ff82d7b68acba38254601fac1a2b8703ca177b32e12f4c08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:35:23 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:35:26 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:35:26 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:35:26 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53d8c63f0ad88bc2d676416ee3944854719f04009c45944d88d5fc62b58a46d2`  
		Last Modified: Mon, 26 Jan 2026 19:35:56 GMT  
		Size: 176.3 MB (176259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfa1d0a816e4d378cf45371b96ba566c4685aaaa97ff23e1b3d7460c5346938`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 8.8 KB (8758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:4e3a1a63a8528a69291e7c55660cade89e8f6d059f29063668aac8697584c097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe11e20c4d32f87d6bbd1d16687621492a2d8f833b9752337d61602987924f8f`

```dockerfile
```

-	Layers:
	-	`sha256:198bbfd8e144914aa40395c9717ce5b4a3222a3ac8308f20f9886f5e875c4ed2`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 8.4 MB (8398819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f941c6325cc9b870babe7067404882ef1c0a36981a131fca2cf27b1ea41ed6e`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260125.0.484595`

```console
$ docker pull archlinux@sha256:3706b9784abbea6c3cae6da206b0f3fb3b7d363408db591604578bc32e022359
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260125.0.484595` - linux; amd64

```console
$ docker pull archlinux@sha256:e4ed0eedd03eae66b22fed7ed701bf2f613006ba53f17cbd7052210b0266eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f60429ea8275a3ff82d7b68acba38254601fac1a2b8703ca177b32e12f4c08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:35:23 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:35:26 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:35:26 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:35:26 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53d8c63f0ad88bc2d676416ee3944854719f04009c45944d88d5fc62b58a46d2`  
		Last Modified: Mon, 26 Jan 2026 19:35:56 GMT  
		Size: 176.3 MB (176259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfa1d0a816e4d378cf45371b96ba566c4685aaaa97ff23e1b3d7460c5346938`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 8.8 KB (8758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260125.0.484595` - unknown; unknown

```console
$ docker pull archlinux@sha256:4e3a1a63a8528a69291e7c55660cade89e8f6d059f29063668aac8697584c097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe11e20c4d32f87d6bbd1d16687621492a2d8f833b9752337d61602987924f8f`

```dockerfile
```

-	Layers:
	-	`sha256:198bbfd8e144914aa40395c9717ce5b4a3222a3ac8308f20f9886f5e875c4ed2`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 8.4 MB (8398819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f941c6325cc9b870babe7067404882ef1c0a36981a131fca2cf27b1ea41ed6e`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:11ce6b24090cb1b5025231b17ab50d144c03612d740224ca3d83a761df120939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0d2ae0be60686321b490b57c9cb90c3f2d64eeb05ffeac4c2faa01907cd72777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293785552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a7e1d583d418cbc0c4eec787b2158a08cb9864c28d36a7792105ea62b964bf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:36:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:36:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:36:57 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:36:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1e89069645e551320191d6ed4f9c08c6914dfd1f3290113122c929bd19065ebc`  
		Last Modified: Mon, 26 Jan 2026 19:37:49 GMT  
		Size: 293.8 MB (293776194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02de33fa295f4b98e030eaec091ef6268afb810d40301ba72f06e3e614f291e7`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:243a1cea567a7f054214e2a5bb0567dc7690980ed60051094b539a8d43691eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bf232cf77f577f1468bde3b59ded88c6497bf2441410b2aa1fb9379db05418`

```dockerfile
```

-	Layers:
	-	`sha256:bb6361dfa11d7e7f02840f746ca77831a128aaa0c4e41ad524cc97b5d3fe5527`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c00a06ef49317dbc918b98288ce7d44c43151e37138212b01e2df96f388be3`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260125.0.484595`

```console
$ docker pull archlinux@sha256:11ce6b24090cb1b5025231b17ab50d144c03612d740224ca3d83a761df120939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260125.0.484595` - linux; amd64

```console
$ docker pull archlinux@sha256:0d2ae0be60686321b490b57c9cb90c3f2d64eeb05ffeac4c2faa01907cd72777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293785552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a7e1d583d418cbc0c4eec787b2158a08cb9864c28d36a7792105ea62b964bf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:36:50 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:36:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:36:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:36:57 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:36:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1e89069645e551320191d6ed4f9c08c6914dfd1f3290113122c929bd19065ebc`  
		Last Modified: Mon, 26 Jan 2026 19:37:49 GMT  
		Size: 293.8 MB (293776194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02de33fa295f4b98e030eaec091ef6268afb810d40301ba72f06e3e614f291e7`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260125.0.484595` - unknown; unknown

```console
$ docker pull archlinux@sha256:243a1cea567a7f054214e2a5bb0567dc7690980ed60051094b539a8d43691eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bf232cf77f577f1468bde3b59ded88c6497bf2441410b2aa1fb9379db05418`

```dockerfile
```

-	Layers:
	-	`sha256:bb6361dfa11d7e7f02840f746ca77831a128aaa0c4e41ad524cc97b5d3fe5527`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c00a06ef49317dbc918b98288ce7d44c43151e37138212b01e2df96f388be3`  
		Last Modified: Mon, 26 Jan 2026 19:37:43 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:3706b9784abbea6c3cae6da206b0f3fb3b7d363408db591604578bc32e022359
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e4ed0eedd03eae66b22fed7ed701bf2f613006ba53f17cbd7052210b0266eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f60429ea8275a3ff82d7b68acba38254601fac1a2b8703ca177b32e12f4c08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:35:23 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:35:26 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:35:26 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:35:26 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53d8c63f0ad88bc2d676416ee3944854719f04009c45944d88d5fc62b58a46d2`  
		Last Modified: Mon, 26 Jan 2026 19:35:56 GMT  
		Size: 176.3 MB (176259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfa1d0a816e4d378cf45371b96ba566c4685aaaa97ff23e1b3d7460c5346938`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 8.8 KB (8758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:4e3a1a63a8528a69291e7c55660cade89e8f6d059f29063668aac8697584c097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe11e20c4d32f87d6bbd1d16687621492a2d8f833b9752337d61602987924f8f`

```dockerfile
```

-	Layers:
	-	`sha256:198bbfd8e144914aa40395c9717ce5b4a3222a3ac8308f20f9886f5e875c4ed2`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 8.4 MB (8398819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f941c6325cc9b870babe7067404882ef1c0a36981a131fca2cf27b1ea41ed6e`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:851211871a857f4c39cc703205f3aa85f2b1a0a9cff021ece26eaf93235e960d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:de3b7b81814d75dac610d07a37c9fd8c3c18a1f39a01953cde0cf0447af0cb74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345103946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fced90a89536058b2bc132e511c546b05d84b700643e992b7e6c32a4d57320`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:36:33 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:36:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:36:41 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:36:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b082aaf37d1f8448ecdf12a68276aa8babba8acde9f2d22a3396b4db41c0684d`  
		Last Modified: Mon, 26 Jan 2026 19:37:38 GMT  
		Size: 345.1 MB (345093462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ade524dd32242b793eb6b3bee4ac59174d6b53eb1308ba36b081931ef571bad`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:083a1414ca8b4ed7962181c42f413b0da2048aceab4152f3d6876a494811693b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12442787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d7e88a2d9fde05a5f7a6079b450d7a69db662ad4727c672d63d0c595fe564f`

```dockerfile
```

-	Layers:
	-	`sha256:38498fe0ce3a3f4c8fa23d7a31d195215881bab55b4cb1bb21f5f07aa40aa3ba`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 12.4 MB (12431019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4760a625a618838fa060efea86e8e33345f1053c49b3e6a7c99482708164a5`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260125.0.484595`

```console
$ docker pull archlinux@sha256:851211871a857f4c39cc703205f3aa85f2b1a0a9cff021ece26eaf93235e960d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260125.0.484595` - linux; amd64

```console
$ docker pull archlinux@sha256:de3b7b81814d75dac610d07a37c9fd8c3c18a1f39a01953cde0cf0447af0cb74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345103946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fced90a89536058b2bc132e511c546b05d84b700643e992b7e6c32a4d57320`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:36:33 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:36:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:36:41 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:36:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b082aaf37d1f8448ecdf12a68276aa8babba8acde9f2d22a3396b4db41c0684d`  
		Last Modified: Mon, 26 Jan 2026 19:37:38 GMT  
		Size: 345.1 MB (345093462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ade524dd32242b793eb6b3bee4ac59174d6b53eb1308ba36b081931ef571bad`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260125.0.484595` - unknown; unknown

```console
$ docker pull archlinux@sha256:083a1414ca8b4ed7962181c42f413b0da2048aceab4152f3d6876a494811693b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12442787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d7e88a2d9fde05a5f7a6079b450d7a69db662ad4727c672d63d0c595fe564f`

```dockerfile
```

-	Layers:
	-	`sha256:38498fe0ce3a3f4c8fa23d7a31d195215881bab55b4cb1bb21f5f07aa40aa3ba`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 12.4 MB (12431019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4760a625a618838fa060efea86e8e33345f1053c49b3e6a7c99482708164a5`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
