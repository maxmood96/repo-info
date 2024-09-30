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
$ docker pull archlinux@sha256:89c27a4ff1d7d36707f480e0a4592c36cf10f10f7a863a0edc25a66150b594ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0f4020e179ffd4ffaeee875e0428db4725a70bad0b19d41a4a67c5ab9ad25a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151192144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37aeb8ca57b911c97101b8d388be4d9d01e2269eb2f8c378a16e27b7cd860cb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240922.0.264758
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-22T00:07:28+00:00
# Sun, 22 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240922.0.264758' /etc/os-release # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:417c3484ea7545ab975fe7bb5b75979245a2dfe8ac68e5440d7a91ed7fc96b91`  
		Last Modified: Tue, 24 Sep 2024 01:00:26 GMT  
		Size: 151.2 MB (151183919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266f74849237343d38f8d4e64d975434645d47398e77a13f83062ff0690f86c7`  
		Last Modified: Tue, 24 Sep 2024 01:00:25 GMT  
		Size: 8.2 KB (8225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:de41d4f09b4f9fc50d5f2d0a649262588cdfd6aff537216de99611aabe5f0b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 KB (11502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2878e7d008da41e32c961fc3f5791e23658da41a32321a0bbdc1554277962662`

```dockerfile
```

-	Layers:
	-	`sha256:769812e6e0b1c94a3b53ad312b9b10ffa81a682d9687c57691904cc75d078164`  
		Last Modified: Tue, 24 Sep 2024 01:00:24 GMT  
		Size: 11.5 KB (11502 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240929.0.266368`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:a723bca84af8678ab536c40d801b2d3e924609eb94fdb68bded2429761d6c936
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e14758c423c552c92c1915cc0eae7b7dec1f02b1e8c6babade9e9faf91621696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272192548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0750879428a1e237572004e17750a9cb040e4156aa1fcfe30dd80bbfead10182`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240922.0.264758
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-22T00:07:28+00:00
# Sun, 22 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240922.0.264758' /etc/os-release # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d6abce642a08032becb5b773d22440c35b58ffd22f076691b2fa3ed896fe4c5a`  
		Last Modified: Tue, 24 Sep 2024 01:00:58 GMT  
		Size: 272.2 MB (272183552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aa93043ad97fe0ac219a3937b67a76fdd71063a8de1fb71ad7bb0ca7dc7693`  
		Last Modified: Tue, 24 Sep 2024 01:00:54 GMT  
		Size: 9.0 KB (8996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f118252b285cedf3f562e9bc839fd22fab98ae5aa994a2617e37d8fe4777ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2cc453bab04b5b001dd69bff7332c5be6f1c0a226acc67a7627af6982c686`

```dockerfile
```

-	Layers:
	-	`sha256:d3c75681fe65dbce30d8ec7dc2797a36440290e1eaf30506c2976d1affb63878`  
		Last Modified: Tue, 24 Sep 2024 01:00:54 GMT  
		Size: 11.3 KB (11283 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240929.0.266368`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:89c27a4ff1d7d36707f480e0a4592c36cf10f10f7a863a0edc25a66150b594ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0f4020e179ffd4ffaeee875e0428db4725a70bad0b19d41a4a67c5ab9ad25a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151192144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37aeb8ca57b911c97101b8d388be4d9d01e2269eb2f8c378a16e27b7cd860cb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240922.0.264758
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-22T00:07:28+00:00
# Sun, 22 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240922.0.264758' /etc/os-release # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:417c3484ea7545ab975fe7bb5b75979245a2dfe8ac68e5440d7a91ed7fc96b91`  
		Last Modified: Tue, 24 Sep 2024 01:00:26 GMT  
		Size: 151.2 MB (151183919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266f74849237343d38f8d4e64d975434645d47398e77a13f83062ff0690f86c7`  
		Last Modified: Tue, 24 Sep 2024 01:00:25 GMT  
		Size: 8.2 KB (8225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:de41d4f09b4f9fc50d5f2d0a649262588cdfd6aff537216de99611aabe5f0b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 KB (11502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2878e7d008da41e32c961fc3f5791e23658da41a32321a0bbdc1554277962662`

```dockerfile
```

-	Layers:
	-	`sha256:769812e6e0b1c94a3b53ad312b9b10ffa81a682d9687c57691904cc75d078164`  
		Last Modified: Tue, 24 Sep 2024 01:00:24 GMT  
		Size: 11.5 KB (11502 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:ddf93aeb00bb0be8dd2aadbd643df87c377e2f8726740303e6c44c7090e10958
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f060ca5c442d84181890d7da8c2aa5e417461284d9bd53349ec382255ac172b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322033407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d25e6dcbb4408f220a503251a6c8f577930f571883648f75e438a244896c006`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240922.0.264758
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-22T00:07:28+00:00
# Sun, 22 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240922.0.264758' /etc/os-release # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:af8cd7f7e1674adbe5034430b3436c5d6f18139c2874c5b6dccc976d10e524cf`  
		Last Modified: Tue, 24 Sep 2024 01:01:02 GMT  
		Size: 322.0 MB (322023290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0728a7a6acfbd344c411fa9b8d285bb2f7a0ca9eed9c8bbe2547b97b79eb0b59`  
		Last Modified: Tue, 24 Sep 2024 01:00:57 GMT  
		Size: 10.1 KB (10117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:418c036fa6b5f6794ec089722431e97abdc54df35ddf8a34bf2b5a338b2dd188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c38cbab71b56f267bf8f4634acf241001255611e093755c4b621d75aaeb18bd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d329deacd452b4bbc1f7a075485844a80c9755f285b2c4c087b1e4ff91383f`  
		Last Modified: Tue, 24 Sep 2024 01:00:57 GMT  
		Size: 11.3 KB (11341 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240929.0.266368`

**does not exist** (yet?)
