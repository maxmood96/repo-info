<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260308.0.497099`](#archlinuxbase-202603080497099)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260308.0.497099`](#archlinuxbase-devel-202603080497099)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260308.0.497099`](#archlinuxmultilib-devel-202603080497099)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:b55ff128e357ad0ce5e0438e2d7bf9b51fb2ce5bdf424109da14ee01c996d571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:19f09c502102d6d249f4e15667144cab1b8a195d9a549996774a665f582bea99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128219437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdcac75cafbee88d88f6fd64e66ee4ddd5750029106ea1c3ea3ca0701466908`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:58:18 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:58:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:58:20 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:58:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c2d2ddabd2750593fbedbe3a807324bb0293c05710ac7366604b7bb762c8beab`  
		Last Modified: Mon, 09 Mar 2026 17:58:46 GMT  
		Size: 128.2 MB (128210860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbb5d4707f913bd2a2dd6d36731fd276df3bbcba701a2e65ca8e51b9161af0a`  
		Last Modified: Mon, 09 Mar 2026 17:58:42 GMT  
		Size: 8.6 KB (8577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:e21eab2861898378f067fbb1318ba56cd00dfe91fdbbd35ca5bc143de85dfbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a66fd005eeabe9ba7e5fa8c8191cec9631f50a9b88a6c6507b6105c13448456`

```dockerfile
```

-	Layers:
	-	`sha256:66713033f586953dd9b84870ec77fe9370b9a1587bc455b3e8aa6c3c0b7e25d4`  
		Last Modified: Mon, 09 Mar 2026 17:58:43 GMT  
		Size: 8.1 MB (8103088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7becf3aa92a9292ffb8398518c58594fa5c5e7ee3a68666832fa666645361e0`  
		Last Modified: Mon, 09 Mar 2026 17:58:42 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260308.0.497099`

```console
$ docker pull archlinux@sha256:b55ff128e357ad0ce5e0438e2d7bf9b51fb2ce5bdf424109da14ee01c996d571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260308.0.497099` - linux; amd64

```console
$ docker pull archlinux@sha256:19f09c502102d6d249f4e15667144cab1b8a195d9a549996774a665f582bea99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128219437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdcac75cafbee88d88f6fd64e66ee4ddd5750029106ea1c3ea3ca0701466908`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:58:18 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:58:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:58:20 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:58:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c2d2ddabd2750593fbedbe3a807324bb0293c05710ac7366604b7bb762c8beab`  
		Last Modified: Mon, 09 Mar 2026 17:58:46 GMT  
		Size: 128.2 MB (128210860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbb5d4707f913bd2a2dd6d36731fd276df3bbcba701a2e65ca8e51b9161af0a`  
		Last Modified: Mon, 09 Mar 2026 17:58:42 GMT  
		Size: 8.6 KB (8577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260308.0.497099` - unknown; unknown

```console
$ docker pull archlinux@sha256:e21eab2861898378f067fbb1318ba56cd00dfe91fdbbd35ca5bc143de85dfbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a66fd005eeabe9ba7e5fa8c8191cec9631f50a9b88a6c6507b6105c13448456`

```dockerfile
```

-	Layers:
	-	`sha256:66713033f586953dd9b84870ec77fe9370b9a1587bc455b3e8aa6c3c0b7e25d4`  
		Last Modified: Mon, 09 Mar 2026 17:58:43 GMT  
		Size: 8.1 MB (8103088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7becf3aa92a9292ffb8398518c58594fa5c5e7ee3a68666832fa666645361e0`  
		Last Modified: Mon, 09 Mar 2026 17:58:42 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b3c1ff749031ca2e06df1cd83fda74df13206a047b7b0f96b818825d9dc60785
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:42a29e6cc13502f8f80cb260300a9c6b1e6008c2308032b98e0c2e3663c6bce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245847356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a733d65c09f048602156757aefd83904a48faff31a7bdc33950e01d12a67ea47`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:59:41 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:59:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:59:47 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:59:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:94a058dd3ee0bc361e3cb4973ff16d37231e1333ac7e7f49783edec0f3468358`  
		Last Modified: Mon, 09 Mar 2026 18:00:31 GMT  
		Size: 245.8 MB (245838229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2199aa76033b1b31fe873642bdbb34e21cf45649d13b5f0137cf27f7fdd98811`  
		Last Modified: Mon, 09 Mar 2026 18:00:27 GMT  
		Size: 9.1 KB (9127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:251f8f567b3250ae10f7489bc177c1eedf5a121c3cd9ce2b696fe17a9a53b7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11897139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb53b193f55d8cc4931c198251c78f1671166490391dea0f46f66af19164a88`

```dockerfile
```

-	Layers:
	-	`sha256:0bc4454778b0713a90c8361ede5789da48af8c4d5762f13effb53005189eeb69`  
		Last Modified: Mon, 09 Mar 2026 18:00:31 GMT  
		Size: 11.9 MB (11885428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf2cb5383c0020b1ca882eec73638a1142eb21363ed263c5acd57721e22b40a`  
		Last Modified: Mon, 09 Mar 2026 18:00:28 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260308.0.497099`

```console
$ docker pull archlinux@sha256:b3c1ff749031ca2e06df1cd83fda74df13206a047b7b0f96b818825d9dc60785
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260308.0.497099` - linux; amd64

```console
$ docker pull archlinux@sha256:42a29e6cc13502f8f80cb260300a9c6b1e6008c2308032b98e0c2e3663c6bce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245847356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a733d65c09f048602156757aefd83904a48faff31a7bdc33950e01d12a67ea47`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:59:41 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:59:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:59:47 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:59:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:94a058dd3ee0bc361e3cb4973ff16d37231e1333ac7e7f49783edec0f3468358`  
		Last Modified: Mon, 09 Mar 2026 18:00:31 GMT  
		Size: 245.8 MB (245838229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2199aa76033b1b31fe873642bdbb34e21cf45649d13b5f0137cf27f7fdd98811`  
		Last Modified: Mon, 09 Mar 2026 18:00:27 GMT  
		Size: 9.1 KB (9127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260308.0.497099` - unknown; unknown

```console
$ docker pull archlinux@sha256:251f8f567b3250ae10f7489bc177c1eedf5a121c3cd9ce2b696fe17a9a53b7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11897139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb53b193f55d8cc4931c198251c78f1671166490391dea0f46f66af19164a88`

```dockerfile
```

-	Layers:
	-	`sha256:0bc4454778b0713a90c8361ede5789da48af8c4d5762f13effb53005189eeb69`  
		Last Modified: Mon, 09 Mar 2026 18:00:31 GMT  
		Size: 11.9 MB (11885428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf2cb5383c0020b1ca882eec73638a1142eb21363ed263c5acd57721e22b40a`  
		Last Modified: Mon, 09 Mar 2026 18:00:28 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:b55ff128e357ad0ce5e0438e2d7bf9b51fb2ce5bdf424109da14ee01c996d571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:19f09c502102d6d249f4e15667144cab1b8a195d9a549996774a665f582bea99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128219437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdcac75cafbee88d88f6fd64e66ee4ddd5750029106ea1c3ea3ca0701466908`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:58:18 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:58:18 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:58:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:58:20 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:58:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c2d2ddabd2750593fbedbe3a807324bb0293c05710ac7366604b7bb762c8beab`  
		Last Modified: Mon, 09 Mar 2026 17:58:46 GMT  
		Size: 128.2 MB (128210860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbb5d4707f913bd2a2dd6d36731fd276df3bbcba701a2e65ca8e51b9161af0a`  
		Last Modified: Mon, 09 Mar 2026 17:58:42 GMT  
		Size: 8.6 KB (8577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:e21eab2861898378f067fbb1318ba56cd00dfe91fdbbd35ca5bc143de85dfbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a66fd005eeabe9ba7e5fa8c8191cec9631f50a9b88a6c6507b6105c13448456`

```dockerfile
```

-	Layers:
	-	`sha256:66713033f586953dd9b84870ec77fe9370b9a1587bc455b3e8aa6c3c0b7e25d4`  
		Last Modified: Mon, 09 Mar 2026 17:58:43 GMT  
		Size: 8.1 MB (8103088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7becf3aa92a9292ffb8398518c58594fa5c5e7ee3a68666832fa666645361e0`  
		Last Modified: Mon, 09 Mar 2026 17:58:42 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:86bcf11a2af9cd87997f08806ca3c2a05d32af3161a9158aae5f95a08eaf019e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:91471305f14d1bed5e4661f35c1429431365c76979b06520790f3812193ad21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268002870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6387a0e3ee19e7bf9612c69de2f89cf273838a7442cefbc9f309e38e1dcb07`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:59:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:59:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:59:31 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:59:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:262510de7e37ef25bb8872186940e06f3b8fce0ed8899d504cf10f7ca2fed259`  
		Last Modified: Mon, 09 Mar 2026 18:00:19 GMT  
		Size: 268.0 MB (267992546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17a20878b942e4b5f45e3f2c37fe8aaa04cc63d08eaa5cae076cd265a8c3e0b`  
		Last Modified: Mon, 09 Mar 2026 18:00:13 GMT  
		Size: 10.3 KB (10324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c846217d0c3212b438bf8c659f05e356aaf026e314ccdfe732d92c72f73ec2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7b5746361122ba377504b95b7d2242b6cbb14a5592ba018e93a514ca14aa13`

```dockerfile
```

-	Layers:
	-	`sha256:89d1b3748bf48a88ab3dd44e22cd192f8541c6cc11475bb606802119ac38fc6c`  
		Last Modified: Mon, 09 Mar 2026 18:00:13 GMT  
		Size: 12.2 MB (12155298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb7b585297a25f362afb00bcb9848679417aa1fdbcee09ea9a13de7fc3c5c9e`  
		Last Modified: Mon, 09 Mar 2026 18:00:14 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260308.0.497099`

```console
$ docker pull archlinux@sha256:86bcf11a2af9cd87997f08806ca3c2a05d32af3161a9158aae5f95a08eaf019e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260308.0.497099` - linux; amd64

```console
$ docker pull archlinux@sha256:91471305f14d1bed5e4661f35c1429431365c76979b06520790f3812193ad21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268002870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6387a0e3ee19e7bf9612c69de2f89cf273838a7442cefbc9f309e38e1dcb07`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:59:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:59:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:59:31 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:59:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:262510de7e37ef25bb8872186940e06f3b8fce0ed8899d504cf10f7ca2fed259`  
		Last Modified: Mon, 09 Mar 2026 18:00:19 GMT  
		Size: 268.0 MB (267992546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17a20878b942e4b5f45e3f2c37fe8aaa04cc63d08eaa5cae076cd265a8c3e0b`  
		Last Modified: Mon, 09 Mar 2026 18:00:13 GMT  
		Size: 10.3 KB (10324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260308.0.497099` - unknown; unknown

```console
$ docker pull archlinux@sha256:c846217d0c3212b438bf8c659f05e356aaf026e314ccdfe732d92c72f73ec2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7b5746361122ba377504b95b7d2242b6cbb14a5592ba018e93a514ca14aa13`

```dockerfile
```

-	Layers:
	-	`sha256:89d1b3748bf48a88ab3dd44e22cd192f8541c6cc11475bb606802119ac38fc6c`  
		Last Modified: Mon, 09 Mar 2026 18:00:13 GMT  
		Size: 12.2 MB (12155298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb7b585297a25f362afb00bcb9848679417aa1fdbcee09ea9a13de7fc3c5c9e`  
		Last Modified: Mon, 09 Mar 2026 18:00:14 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
