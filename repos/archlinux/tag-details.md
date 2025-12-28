<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20251228.0.475343`](#archlinuxbase-202512280475343)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20251228.0.475343`](#archlinuxbase-devel-202512280475343)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20251228.0.475343`](#archlinuxmultilib-devel-202512280475343)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:f7047b912073aba008a42602920728e3fd604f4a1b50ae35babd64012eba5b3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:5e0f5cc5dea069631fd7063d8d30882d279e284eb6a55a6b78914b3445c3cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174700424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c7824611c1e76660613ebde66b59a3c8965835deff9dc6def42b1f6b16a0d1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.version=20251228.0.475343
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.created=2025-12-28T00:07:28+00:00
# Sun, 28 Dec 2025 06:06:03 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Dec 2025 06:06:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251228.0.475343' /etc/os-release # buildkit
# Sun, 28 Dec 2025 06:06:07 GMT
ENV LANG=C.UTF-8
# Sun, 28 Dec 2025 06:06:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:20d00f72b79fb24dbc6809112d9f7af7c8e303260a68a34699df7debbe244cda`  
		Last Modified: Sun, 28 Dec 2025 06:09:10 GMT  
		Size: 174.7 MB (174691727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e25fa94686e93ca5d8c96753ab861942fb0e62701bb4e25806ed358f60cc8df`  
		Last Modified: Sun, 28 Dec 2025 06:06:43 GMT  
		Size: 8.7 KB (8697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:9621c043bf27a43a7a4f0a6a9446261f48068c82c9bbfaa97b6c646c76e168d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ca384f9d88b5fdb2ae1a46e8ae193b04757351ac138a48a90ea13f9621e5e6`

```dockerfile
```

-	Layers:
	-	`sha256:1450f3524fffd7ad7f729c1e25460403b290f24131544f9040c734d5d1067186`  
		Last Modified: Sun, 28 Dec 2025 08:48:17 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc0bf1a8c3b9d44b27a406ff08950e644a63d4eb25cd1bc9b105accc25e73c5`  
		Last Modified: Sun, 28 Dec 2025 08:48:18 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251228.0.475343`

```console
$ docker pull archlinux@sha256:f7047b912073aba008a42602920728e3fd604f4a1b50ae35babd64012eba5b3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20251228.0.475343` - linux; amd64

```console
$ docker pull archlinux@sha256:5e0f5cc5dea069631fd7063d8d30882d279e284eb6a55a6b78914b3445c3cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174700424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c7824611c1e76660613ebde66b59a3c8965835deff9dc6def42b1f6b16a0d1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.version=20251228.0.475343
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.created=2025-12-28T00:07:28+00:00
# Sun, 28 Dec 2025 06:06:03 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Dec 2025 06:06:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251228.0.475343' /etc/os-release # buildkit
# Sun, 28 Dec 2025 06:06:07 GMT
ENV LANG=C.UTF-8
# Sun, 28 Dec 2025 06:06:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:20d00f72b79fb24dbc6809112d9f7af7c8e303260a68a34699df7debbe244cda`  
		Last Modified: Sun, 28 Dec 2025 06:09:10 GMT  
		Size: 174.7 MB (174691727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e25fa94686e93ca5d8c96753ab861942fb0e62701bb4e25806ed358f60cc8df`  
		Last Modified: Sun, 28 Dec 2025 06:06:43 GMT  
		Size: 8.7 KB (8697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20251228.0.475343` - unknown; unknown

```console
$ docker pull archlinux@sha256:9621c043bf27a43a7a4f0a6a9446261f48068c82c9bbfaa97b6c646c76e168d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ca384f9d88b5fdb2ae1a46e8ae193b04757351ac138a48a90ea13f9621e5e6`

```dockerfile
```

-	Layers:
	-	`sha256:1450f3524fffd7ad7f729c1e25460403b290f24131544f9040c734d5d1067186`  
		Last Modified: Sun, 28 Dec 2025 08:48:17 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc0bf1a8c3b9d44b27a406ff08950e644a63d4eb25cd1bc9b105accc25e73c5`  
		Last Modified: Sun, 28 Dec 2025 08:48:18 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:f6b259c6c0cd1bc4c86510485acb6a5f053c15789c9c68c7434b6fe99564906c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f7a012126cb4a9fa7b5ac521a6fc38f14c6c697048baddc3406484b6c5d392af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292240861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c9b98f502d34c4c415ecd55d2e0c001ca669aa4ca8fa2e8ce4a0df629db8d3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.version=20251228.0.475343
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.created=2025-12-28T00:07:28+00:00
# Sun, 28 Dec 2025 06:06:19 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Dec 2025 06:06:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251228.0.475343' /etc/os-release # buildkit
# Sun, 28 Dec 2025 06:06:25 GMT
ENV LANG=C.UTF-8
# Sun, 28 Dec 2025 06:06:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:bf1232cf64d2a9da3fde760d090738010168efc08a23e9a8315879e3936e4b97`  
		Last Modified: Sun, 28 Dec 2025 06:08:35 GMT  
		Size: 292.2 MB (292231673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91507c1e8a5c4cadb79de899486608dbf84b0d651ebc96d20c8f736ca8cf8ce3`  
		Last Modified: Sun, 28 Dec 2025 06:07:20 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:cd56966fe48bf1a9438f362e14b12b275a36d3bb79224ef44142a59eb51347a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12157441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d534565e3be73b4de3bfe87b7fbd5149fe953659b71b1ca6620786f2e3f9afc`

```dockerfile
```

-	Layers:
	-	`sha256:b13dc36d0a1c7637aebbaf4527e12f06045a403cd3ed19a304d21ed1e2f8f047`  
		Last Modified: Sun, 28 Dec 2025 08:48:23 GMT  
		Size: 12.1 MB (12145730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:494860e8a71287c642d4a0fdf373ab1534f0db43428d3f7e44ccd988276126f3`  
		Last Modified: Sun, 28 Dec 2025 08:48:24 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251228.0.475343`

```console
$ docker pull archlinux@sha256:f6b259c6c0cd1bc4c86510485acb6a5f053c15789c9c68c7434b6fe99564906c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251228.0.475343` - linux; amd64

```console
$ docker pull archlinux@sha256:f7a012126cb4a9fa7b5ac521a6fc38f14c6c697048baddc3406484b6c5d392af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292240861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c9b98f502d34c4c415ecd55d2e0c001ca669aa4ca8fa2e8ce4a0df629db8d3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.version=20251228.0.475343
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Sun, 28 Dec 2025 06:06:19 GMT
LABEL org.opencontainers.image.created=2025-12-28T00:07:28+00:00
# Sun, 28 Dec 2025 06:06:19 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Dec 2025 06:06:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251228.0.475343' /etc/os-release # buildkit
# Sun, 28 Dec 2025 06:06:25 GMT
ENV LANG=C.UTF-8
# Sun, 28 Dec 2025 06:06:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:bf1232cf64d2a9da3fde760d090738010168efc08a23e9a8315879e3936e4b97`  
		Last Modified: Sun, 28 Dec 2025 06:08:35 GMT  
		Size: 292.2 MB (292231673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91507c1e8a5c4cadb79de899486608dbf84b0d651ebc96d20c8f736ca8cf8ce3`  
		Last Modified: Sun, 28 Dec 2025 06:07:20 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251228.0.475343` - unknown; unknown

```console
$ docker pull archlinux@sha256:cd56966fe48bf1a9438f362e14b12b275a36d3bb79224ef44142a59eb51347a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12157441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d534565e3be73b4de3bfe87b7fbd5149fe953659b71b1ca6620786f2e3f9afc`

```dockerfile
```

-	Layers:
	-	`sha256:b13dc36d0a1c7637aebbaf4527e12f06045a403cd3ed19a304d21ed1e2f8f047`  
		Last Modified: Sun, 28 Dec 2025 08:48:23 GMT  
		Size: 12.1 MB (12145730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:494860e8a71287c642d4a0fdf373ab1534f0db43428d3f7e44ccd988276126f3`  
		Last Modified: Sun, 28 Dec 2025 08:48:24 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:f7047b912073aba008a42602920728e3fd604f4a1b50ae35babd64012eba5b3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:5e0f5cc5dea069631fd7063d8d30882d279e284eb6a55a6b78914b3445c3cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174700424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c7824611c1e76660613ebde66b59a3c8965835deff9dc6def42b1f6b16a0d1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.version=20251228.0.475343
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Sun, 28 Dec 2025 06:06:03 GMT
LABEL org.opencontainers.image.created=2025-12-28T00:07:28+00:00
# Sun, 28 Dec 2025 06:06:03 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Dec 2025 06:06:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251228.0.475343' /etc/os-release # buildkit
# Sun, 28 Dec 2025 06:06:07 GMT
ENV LANG=C.UTF-8
# Sun, 28 Dec 2025 06:06:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:20d00f72b79fb24dbc6809112d9f7af7c8e303260a68a34699df7debbe244cda`  
		Last Modified: Sun, 28 Dec 2025 06:09:10 GMT  
		Size: 174.7 MB (174691727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e25fa94686e93ca5d8c96753ab861942fb0e62701bb4e25806ed358f60cc8df`  
		Last Modified: Sun, 28 Dec 2025 06:06:43 GMT  
		Size: 8.7 KB (8697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:9621c043bf27a43a7a4f0a6a9446261f48068c82c9bbfaa97b6c646c76e168d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ca384f9d88b5fdb2ae1a46e8ae193b04757351ac138a48a90ea13f9621e5e6`

```dockerfile
```

-	Layers:
	-	`sha256:1450f3524fffd7ad7f729c1e25460403b290f24131544f9040c734d5d1067186`  
		Last Modified: Sun, 28 Dec 2025 08:48:17 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc0bf1a8c3b9d44b27a406ff08950e644a63d4eb25cd1bc9b105accc25e73c5`  
		Last Modified: Sun, 28 Dec 2025 08:48:18 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:604fccf6283d42ea730a9d529ca0fae86ac3e45e46cf174a2fd9b7106c74ba66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:97b57d96e956c96abc53c08ce4fd79bbdac22c559c6c9d56057f00cce49bb9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343557638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777c0ca8979ac84d7c4e6a2840cb08c885090f0164971d71fd328c8a9fe807b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.version=20251228.0.475343
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.created=2025-12-28T00:07:28+00:00
# Sun, 28 Dec 2025 06:06:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Dec 2025 06:06:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251228.0.475343' /etc/os-release # buildkit
# Sun, 28 Dec 2025 06:06:35 GMT
ENV LANG=C.UTF-8
# Sun, 28 Dec 2025 06:06:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6a0bb30a4ccec874efca15569e0fff6d09a9e1af5958081f4d046eaea43d7141`  
		Last Modified: Sun, 28 Dec 2025 06:07:58 GMT  
		Size: 343.5 MB (343547334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c8a8d2b418cba295d04ef814183f4188be9bbbed25d599f9078c2f206cc58`  
		Last Modified: Sun, 28 Dec 2025 06:07:36 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a484d17b7fff752e73a82ef84f4abbede35b29fd0f5baa6fd764dafd8630fa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1590c89d0bbfcca9a3e920d247621b5dcc217175f73fc0d574b0f9a8ccdb4446`

```dockerfile
```

-	Layers:
	-	`sha256:1aa9efdcaf1769a73d19dba0780948aef1b4687b23076f870b4db120936dd066`  
		Last Modified: Sun, 28 Dec 2025 08:48:29 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b471fde77527b03de17b6541da89d06397a33c20a19f90da2d77fc995c58ff`  
		Last Modified: Sun, 28 Dec 2025 08:48:30 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251228.0.475343`

```console
$ docker pull archlinux@sha256:604fccf6283d42ea730a9d529ca0fae86ac3e45e46cf174a2fd9b7106c74ba66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251228.0.475343` - linux; amd64

```console
$ docker pull archlinux@sha256:97b57d96e956c96abc53c08ce4fd79bbdac22c559c6c9d56057f00cce49bb9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343557638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777c0ca8979ac84d7c4e6a2840cb08c885090f0164971d71fd328c8a9fe807b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.version=20251228.0.475343
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.created=2025-12-28T00:07:28+00:00
# Sun, 28 Dec 2025 06:06:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Dec 2025 06:06:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251228.0.475343' /etc/os-release # buildkit
# Sun, 28 Dec 2025 06:06:35 GMT
ENV LANG=C.UTF-8
# Sun, 28 Dec 2025 06:06:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6a0bb30a4ccec874efca15569e0fff6d09a9e1af5958081f4d046eaea43d7141`  
		Last Modified: Sun, 28 Dec 2025 06:07:58 GMT  
		Size: 343.5 MB (343547334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c8a8d2b418cba295d04ef814183f4188be9bbbed25d599f9078c2f206cc58`  
		Last Modified: Sun, 28 Dec 2025 06:07:36 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251228.0.475343` - unknown; unknown

```console
$ docker pull archlinux@sha256:a484d17b7fff752e73a82ef84f4abbede35b29fd0f5baa6fd764dafd8630fa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1590c89d0bbfcca9a3e920d247621b5dcc217175f73fc0d574b0f9a8ccdb4446`

```dockerfile
```

-	Layers:
	-	`sha256:1aa9efdcaf1769a73d19dba0780948aef1b4687b23076f870b4db120936dd066`  
		Last Modified: Sun, 28 Dec 2025 08:48:29 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b471fde77527b03de17b6541da89d06397a33c20a19f90da2d77fc995c58ff`  
		Last Modified: Sun, 28 Dec 2025 08:48:30 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
