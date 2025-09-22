<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250921.0.423275`](#archlinuxbase-202509210423275)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250921.0.423275`](#archlinuxbase-devel-202509210423275)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250921.0.423275`](#archlinuxmultilib-devel-202509210423275)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:2eb1a56a6036b1f70e63ca714814fe304a8f20d29ab425b4f056f34508500000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:16a95721ca6e63048ca1ca960b4ac8d9a5c74609d46954ef792a5e1360f41069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164710165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffd4a0cbb9673a6d6364ffef73b1627819f21c569710dadfa7a8a8273f35e52`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:178f25afaa61842b62d72a1943af8d3e78aee9a28649f53b0d2bdfce5c3620c4`  
		Last Modified: Mon, 22 Sep 2025 16:51:27 GMT  
		Size: 164.7 MB (164701824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc5f4896ee5f282a483cf3bdfa35a12103e2d5bc65dde7d05ba31808f47ca4`  
		Last Modified: Mon, 22 Sep 2025 16:51:13 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:41822909d08eb83c13857b357f83b78d0425370d34b34243713c362d5d2acce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0591214c03fac9c8bc073cf5d069f47bd2cf3dd0b7f8e615ea9a9508047d2240`

```dockerfile
```

-	Layers:
	-	`sha256:6697f22c06f0934acaef7765347f2a10a3072be97462c9990fc15769d9363182`  
		Last Modified: Mon, 22 Sep 2025 19:48:17 GMT  
		Size: 8.2 MB (8217061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c3ab3330f5682f771e21732c823f450549a383ab6c5dbb58934cc7278f014b`  
		Last Modified: Mon, 22 Sep 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250921.0.423275`

```console
$ docker pull archlinux@sha256:2eb1a56a6036b1f70e63ca714814fe304a8f20d29ab425b4f056f34508500000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250921.0.423275` - linux; amd64

```console
$ docker pull archlinux@sha256:16a95721ca6e63048ca1ca960b4ac8d9a5c74609d46954ef792a5e1360f41069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164710165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffd4a0cbb9673a6d6364ffef73b1627819f21c569710dadfa7a8a8273f35e52`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:178f25afaa61842b62d72a1943af8d3e78aee9a28649f53b0d2bdfce5c3620c4`  
		Last Modified: Mon, 22 Sep 2025 16:51:27 GMT  
		Size: 164.7 MB (164701824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc5f4896ee5f282a483cf3bdfa35a12103e2d5bc65dde7d05ba31808f47ca4`  
		Last Modified: Mon, 22 Sep 2025 16:51:13 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250921.0.423275` - unknown; unknown

```console
$ docker pull archlinux@sha256:41822909d08eb83c13857b357f83b78d0425370d34b34243713c362d5d2acce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0591214c03fac9c8bc073cf5d069f47bd2cf3dd0b7f8e615ea9a9508047d2240`

```dockerfile
```

-	Layers:
	-	`sha256:6697f22c06f0934acaef7765347f2a10a3072be97462c9990fc15769d9363182`  
		Last Modified: Mon, 22 Sep 2025 19:48:17 GMT  
		Size: 8.2 MB (8217061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c3ab3330f5682f771e21732c823f450549a383ab6c5dbb58934cc7278f014b`  
		Last Modified: Mon, 22 Sep 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0589aa8f31d8f64c630a2d1cc0b4c3847a1a63c988abd63d78d3c9bd94764f64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f1e466354b09be5e39c3c776436ea23407fe3d9fdbc0909b9e1e1cdb07fff006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289784440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc65acfd58b235826af8c7dd44a1e845dc3c3f6a9afcbd53492b85897b0a649`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8f0661e86a4352a5b41461a186a2ef2918ccfda12cf00f17378f3b5ccaa68223`  
		Last Modified: Mon, 22 Sep 2025 19:52:56 GMT  
		Size: 289.8 MB (289775279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5d2d390041c4c695fd932609a8370c07aba9831b0a94c06d0ba07bf269e5d4`  
		Last Modified: Mon, 22 Sep 2025 16:53:07 GMT  
		Size: 9.2 KB (9161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d884c4c9df27612319f2ccdb141cef3683df392c89e658c0d48e8d6be96fa9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490a6ecb8ba6e8348eef396e995f4932eceb54df33b0fa9ee097c9edf946ac7`

```dockerfile
```

-	Layers:
	-	`sha256:2eff59a3d6270a9bfa995791356d63c4c2970b85cbda690ec76f8b81d0bf40e9`  
		Last Modified: Mon, 22 Sep 2025 19:48:23 GMT  
		Size: 12.1 MB (12118397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eae29ffd01c3fced7c68f387fbb9a16f93228397b7c237212f826eda99586f0`  
		Last Modified: Mon, 22 Sep 2025 19:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250921.0.423275`

```console
$ docker pull archlinux@sha256:0589aa8f31d8f64c630a2d1cc0b4c3847a1a63c988abd63d78d3c9bd94764f64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250921.0.423275` - linux; amd64

```console
$ docker pull archlinux@sha256:f1e466354b09be5e39c3c776436ea23407fe3d9fdbc0909b9e1e1cdb07fff006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289784440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc65acfd58b235826af8c7dd44a1e845dc3c3f6a9afcbd53492b85897b0a649`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8f0661e86a4352a5b41461a186a2ef2918ccfda12cf00f17378f3b5ccaa68223`  
		Last Modified: Mon, 22 Sep 2025 19:52:56 GMT  
		Size: 289.8 MB (289775279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5d2d390041c4c695fd932609a8370c07aba9831b0a94c06d0ba07bf269e5d4`  
		Last Modified: Mon, 22 Sep 2025 16:53:07 GMT  
		Size: 9.2 KB (9161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250921.0.423275` - unknown; unknown

```console
$ docker pull archlinux@sha256:d884c4c9df27612319f2ccdb141cef3683df392c89e658c0d48e8d6be96fa9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490a6ecb8ba6e8348eef396e995f4932eceb54df33b0fa9ee097c9edf946ac7`

```dockerfile
```

-	Layers:
	-	`sha256:2eff59a3d6270a9bfa995791356d63c4c2970b85cbda690ec76f8b81d0bf40e9`  
		Last Modified: Mon, 22 Sep 2025 19:48:23 GMT  
		Size: 12.1 MB (12118397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eae29ffd01c3fced7c68f387fbb9a16f93228397b7c237212f826eda99586f0`  
		Last Modified: Mon, 22 Sep 2025 19:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:2eb1a56a6036b1f70e63ca714814fe304a8f20d29ab425b4f056f34508500000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:16a95721ca6e63048ca1ca960b4ac8d9a5c74609d46954ef792a5e1360f41069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164710165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffd4a0cbb9673a6d6364ffef73b1627819f21c569710dadfa7a8a8273f35e52`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:178f25afaa61842b62d72a1943af8d3e78aee9a28649f53b0d2bdfce5c3620c4`  
		Last Modified: Mon, 22 Sep 2025 16:51:27 GMT  
		Size: 164.7 MB (164701824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc5f4896ee5f282a483cf3bdfa35a12103e2d5bc65dde7d05ba31808f47ca4`  
		Last Modified: Mon, 22 Sep 2025 16:51:13 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:41822909d08eb83c13857b357f83b78d0425370d34b34243713c362d5d2acce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0591214c03fac9c8bc073cf5d069f47bd2cf3dd0b7f8e615ea9a9508047d2240`

```dockerfile
```

-	Layers:
	-	`sha256:6697f22c06f0934acaef7765347f2a10a3072be97462c9990fc15769d9363182`  
		Last Modified: Mon, 22 Sep 2025 19:48:17 GMT  
		Size: 8.2 MB (8217061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c3ab3330f5682f771e21732c823f450549a383ab6c5dbb58934cc7278f014b`  
		Last Modified: Mon, 22 Sep 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:597974c156be3b466a0cedb0b450766bd829662454545e3289221dfe876dbc21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0e001ad3f885fe9513e544ea99b312a3eae37d8215fee826b5dc84f9af5c14f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341113550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f03b1918cd1635881b2693dd1b8be969a7d45a37560f5b65e34a810339df5a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:05c59540b3238557a896596168f7d03a73c3f68ec38fe506f2d8a4284d8d06e9`  
		Last Modified: Mon, 22 Sep 2025 20:02:38 GMT  
		Size: 341.1 MB (341103287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda24d2c9dd8dcb2064b1b05f2e896214bf788520ebc8622cdc250c3e2eee16d`  
		Last Modified: Mon, 22 Sep 2025 16:53:05 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c14fa21d2076c22888d3c2799f718653b8b22fb928390218d5fc83bb32b4fad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12398996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608e18bff9222928a445bccd1dd3350c3ffdba686fd848795802d32667c4c275`

```dockerfile
```

-	Layers:
	-	`sha256:810bcf02a4239cc21e8393bdca5be31c4b112888d9db15e188606b500977deef`  
		Last Modified: Mon, 22 Sep 2025 19:48:31 GMT  
		Size: 12.4 MB (12387185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ab221638ce572d95472f09d6d451b6198e8c82171f00824664d9f40ed3a3f0`  
		Last Modified: Mon, 22 Sep 2025 19:48:32 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250921.0.423275`

```console
$ docker pull archlinux@sha256:597974c156be3b466a0cedb0b450766bd829662454545e3289221dfe876dbc21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250921.0.423275` - linux; amd64

```console
$ docker pull archlinux@sha256:0e001ad3f885fe9513e544ea99b312a3eae37d8215fee826b5dc84f9af5c14f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341113550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f03b1918cd1635881b2693dd1b8be969a7d45a37560f5b65e34a810339df5a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:05c59540b3238557a896596168f7d03a73c3f68ec38fe506f2d8a4284d8d06e9`  
		Last Modified: Mon, 22 Sep 2025 20:02:38 GMT  
		Size: 341.1 MB (341103287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda24d2c9dd8dcb2064b1b05f2e896214bf788520ebc8622cdc250c3e2eee16d`  
		Last Modified: Mon, 22 Sep 2025 16:53:05 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250921.0.423275` - unknown; unknown

```console
$ docker pull archlinux@sha256:c14fa21d2076c22888d3c2799f718653b8b22fb928390218d5fc83bb32b4fad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12398996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608e18bff9222928a445bccd1dd3350c3ffdba686fd848795802d32667c4c275`

```dockerfile
```

-	Layers:
	-	`sha256:810bcf02a4239cc21e8393bdca5be31c4b112888d9db15e188606b500977deef`  
		Last Modified: Mon, 22 Sep 2025 19:48:31 GMT  
		Size: 12.4 MB (12387185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ab221638ce572d95472f09d6d451b6198e8c82171f00824664d9f40ed3a3f0`  
		Last Modified: Mon, 22 Sep 2025 19:48:32 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
