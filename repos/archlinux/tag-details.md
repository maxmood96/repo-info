<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240101.0.204074`](#archlinuxbase-202401010204074)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240101.0.204074`](#archlinuxbase-devel-202401010204074)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240101.0.204074`](#archlinuxmultilib-devel-202401010204074)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:7ddb28e525cda55998a80d147967865193d170b0cf75c999ff2e3116d8f95a32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:7b5aa07f86a6958bb072227e18e76ef37e59c65bff56a45aab695def2ddecd64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fa6eaece3899bac1ab0691353fb328faf435634a0c82d1c88c28a504cb4ab2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9884827b07bb5df1be9734d10e7db68899aedbb38552f40a11adf399debdaaf`  
		Last Modified: Wed, 08 May 2024 21:11:13 GMT  
		Size: 148.0 MB (147987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9688c28db8a0d21798afbc20a23e0aadbd14555ae21887d45c163c68d3d3042`  
		Last Modified: Thu, 20 Jun 2024 20:55:11 GMT  
		Size: 8.1 KB (8129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:edd980ef21dd76a28f8dfe72bb908a399dc7f2c4d5eab344d6628425531ed009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7958197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501496497dd59052086180961a0179bcea141bf4a3f609cc0bc5bb1c9c7e0743`

```dockerfile
```

-	Layers:
	-	`sha256:1c0a8beb9dde291cfa74a6db9f2d39b1234b54c1c06c229ee48cd020680c3acb`  
		Last Modified: Thu, 20 Jun 2024 20:55:12 GMT  
		Size: 7.9 MB (7946476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcad92faec2ae7ecdcfa6fff658061c3b359bbfa206c9b348cc76f28c361e165`  
		Last Modified: Thu, 20 Jun 2024 20:55:11 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240101.0.204074`

```console
$ docker pull archlinux@sha256:7ddb28e525cda55998a80d147967865193d170b0cf75c999ff2e3116d8f95a32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:7b5aa07f86a6958bb072227e18e76ef37e59c65bff56a45aab695def2ddecd64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fa6eaece3899bac1ab0691353fb328faf435634a0c82d1c88c28a504cb4ab2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9884827b07bb5df1be9734d10e7db68899aedbb38552f40a11adf399debdaaf`  
		Last Modified: Wed, 08 May 2024 21:11:13 GMT  
		Size: 148.0 MB (147987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9688c28db8a0d21798afbc20a23e0aadbd14555ae21887d45c163c68d3d3042`  
		Last Modified: Thu, 20 Jun 2024 20:55:11 GMT  
		Size: 8.1 KB (8129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20240101.0.204074` - unknown; unknown

```console
$ docker pull archlinux@sha256:edd980ef21dd76a28f8dfe72bb908a399dc7f2c4d5eab344d6628425531ed009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7958197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501496497dd59052086180961a0179bcea141bf4a3f609cc0bc5bb1c9c7e0743`

```dockerfile
```

-	Layers:
	-	`sha256:1c0a8beb9dde291cfa74a6db9f2d39b1234b54c1c06c229ee48cd020680c3acb`  
		Last Modified: Thu, 20 Jun 2024 20:55:12 GMT  
		Size: 7.9 MB (7946476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcad92faec2ae7ecdcfa6fff658061c3b359bbfa206c9b348cc76f28c361e165`  
		Last Modified: Thu, 20 Jun 2024 20:55:11 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:4d4821711ba77904458da94ad3db7de44184c6945eb684f96438fe7778b2420f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c65736805583204ee36b28b34aa7106df9e45b35ae545a53ebe5b771171a3e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172c561b410c36e9c5d15433c5f5b359492bffd07b3156ea99b13a0ed08e8519`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad59c724b2d7e7041a88eae078be10f472732091bab7b3ff59e2bbd5056e65f6`  
		Last Modified: Wed, 29 May 2024 19:57:22 GMT  
		Size: 266.2 MB (266230027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdeb6c4b76bd400e6456522b9754397780a2bd2609e44734011239bb5b12f0e`  
		Last Modified: Thu, 20 Jun 2024 20:55:35 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:03ea318b897f20062c906641fee669eafa6b82b12156a6e81e1bc1d98a82aa74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11620644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428ac9355b664ed047a7eb9b6f0d8fc1dacbb8920578be8a8cd377e9d4e3f273`

```dockerfile
```

-	Layers:
	-	`sha256:c6bfffb25a24756dd9a6b4415f9a6ebed5af1f320f13f220ddb9a139aa52fc89`  
		Last Modified: Thu, 20 Jun 2024 20:55:35 GMT  
		Size: 11.6 MB (11609141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d7f8265cb5ae91996336b2febf54bda9ca777299dcabf5e0bee41f2d995651`  
		Last Modified: Thu, 20 Jun 2024 20:55:34 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:4d4821711ba77904458da94ad3db7de44184c6945eb684f96438fe7778b2420f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:c65736805583204ee36b28b34aa7106df9e45b35ae545a53ebe5b771171a3e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172c561b410c36e9c5d15433c5f5b359492bffd07b3156ea99b13a0ed08e8519`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad59c724b2d7e7041a88eae078be10f472732091bab7b3ff59e2bbd5056e65f6`  
		Last Modified: Wed, 29 May 2024 19:57:22 GMT  
		Size: 266.2 MB (266230027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdeb6c4b76bd400e6456522b9754397780a2bd2609e44734011239bb5b12f0e`  
		Last Modified: Thu, 20 Jun 2024 20:55:35 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240101.0.204074` - unknown; unknown

```console
$ docker pull archlinux@sha256:03ea318b897f20062c906641fee669eafa6b82b12156a6e81e1bc1d98a82aa74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11620644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428ac9355b664ed047a7eb9b6f0d8fc1dacbb8920578be8a8cd377e9d4e3f273`

```dockerfile
```

-	Layers:
	-	`sha256:c6bfffb25a24756dd9a6b4415f9a6ebed5af1f320f13f220ddb9a139aa52fc89`  
		Last Modified: Thu, 20 Jun 2024 20:55:35 GMT  
		Size: 11.6 MB (11609141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d7f8265cb5ae91996336b2febf54bda9ca777299dcabf5e0bee41f2d995651`  
		Last Modified: Thu, 20 Jun 2024 20:55:34 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:7ddb28e525cda55998a80d147967865193d170b0cf75c999ff2e3116d8f95a32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:7b5aa07f86a6958bb072227e18e76ef37e59c65bff56a45aab695def2ddecd64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fa6eaece3899bac1ab0691353fb328faf435634a0c82d1c88c28a504cb4ab2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9884827b07bb5df1be9734d10e7db68899aedbb38552f40a11adf399debdaaf`  
		Last Modified: Wed, 08 May 2024 21:11:13 GMT  
		Size: 148.0 MB (147987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9688c28db8a0d21798afbc20a23e0aadbd14555ae21887d45c163c68d3d3042`  
		Last Modified: Thu, 20 Jun 2024 20:55:11 GMT  
		Size: 8.1 KB (8129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:edd980ef21dd76a28f8dfe72bb908a399dc7f2c4d5eab344d6628425531ed009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7958197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501496497dd59052086180961a0179bcea141bf4a3f609cc0bc5bb1c9c7e0743`

```dockerfile
```

-	Layers:
	-	`sha256:1c0a8beb9dde291cfa74a6db9f2d39b1234b54c1c06c229ee48cd020680c3acb`  
		Last Modified: Thu, 20 Jun 2024 20:55:12 GMT  
		Size: 7.9 MB (7946476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcad92faec2ae7ecdcfa6fff658061c3b359bbfa206c9b348cc76f28c361e165`  
		Last Modified: Thu, 20 Jun 2024 20:55:11 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9af24109ecfd2ad28a671b60339ec5aa04175a8bc3b1ed62627f7f863a2d5447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f460c106c5d1615b6f1b8c14c3d0319b18dd392ea02bc07c1a428dd439c94f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316042490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78aa48b5f0c7aee075ed233131704097080f29e2f7848188f3d42a26c420b03f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35515117493e52c38adb77412e5d70e1c716a60977e0d1bad3b1ed7e46700be3`  
		Last Modified: Wed, 29 May 2024 19:57:38 GMT  
		Size: 316.0 MB (316032410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb0b4faa739fd457842297c3fb0985f236ed38fc608e05d3005c0c580335c3`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 10.1 KB (10080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:db257f729b69366a7567c71548db340876c5758cd4bdb240cb0c2ad404fc877b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11887002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bb3b23fe40aa145c11e55cfce61382b3052408f1bf3a4e79eb8fe3ba5d11d9`

```dockerfile
```

-	Layers:
	-	`sha256:1d6130046940a135ea4800a943cb3a126ffae3c87470f1c98efce450541ec75a`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 11.9 MB (11875442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a64d29207bcc3b3262247db9bad2b94a39ec29f9f57114a773bc023299199aa`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:9af24109ecfd2ad28a671b60339ec5aa04175a8bc3b1ed62627f7f863a2d5447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:f460c106c5d1615b6f1b8c14c3d0319b18dd392ea02bc07c1a428dd439c94f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316042490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78aa48b5f0c7aee075ed233131704097080f29e2f7848188f3d42a26c420b03f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35515117493e52c38adb77412e5d70e1c716a60977e0d1bad3b1ed7e46700be3`  
		Last Modified: Wed, 29 May 2024 19:57:38 GMT  
		Size: 316.0 MB (316032410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb0b4faa739fd457842297c3fb0985f236ed38fc608e05d3005c0c580335c3`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 10.1 KB (10080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240101.0.204074` - unknown; unknown

```console
$ docker pull archlinux@sha256:db257f729b69366a7567c71548db340876c5758cd4bdb240cb0c2ad404fc877b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11887002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bb3b23fe40aa145c11e55cfce61382b3052408f1bf3a4e79eb8fe3ba5d11d9`

```dockerfile
```

-	Layers:
	-	`sha256:1d6130046940a135ea4800a943cb3a126ffae3c87470f1c98efce450541ec75a`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 11.9 MB (11875442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a64d29207bcc3b3262247db9bad2b94a39ec29f9f57114a773bc023299199aa`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
