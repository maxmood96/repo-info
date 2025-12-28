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
