<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240721.0.248532`](#archlinuxbase-202407210248532)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240721.0.248532`](#archlinuxbase-devel-202407210248532)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240721.0.248532`](#archlinuxmultilib-devel-202407210248532)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:4c53f5cc2575b95b1e93b8dea77b093b2bb95e8d38ca9500b01563de01112d5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:76b4733d4c59cdfcae4a5dced7a6611e8621a502f863631328b362c85ac405c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151081420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071006412c8f62de399d19fafc32bbbfb4df0838e00c098d8bfbeaea3aa6028f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20240714.0.246936
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-07-14T00:07:41+00:00
# Sun, 14 Jul 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240714.0.246936' /etc/os-release # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 14 Jul 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ca363af79b68bf0121632c656d6df30aa97d5a2f1dde5cc230de91515db1bdc1`  
		Last Modified: Mon, 15 Jul 2024 19:55:31 GMT  
		Size: 151.1 MB (151073152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03dd7efb6b9c81c4f2a3560da6bd744bfbf58456182314f5d8ff66925b75e2b`  
		Last Modified: Mon, 15 Jul 2024 19:55:28 GMT  
		Size: 8.3 KB (8268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:6f7b67160aa0c785c38c5e9c5ee1d515e3c2d92ad59efa322d683a083305075b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb8f781d80ef66dbd3646384c2606f28740566d201f5492373b44a2ae06a9a1`

```dockerfile
```

-	Layers:
	-	`sha256:2c3d83448b05a7e33d48f2a52313ffcd4b3c277e9653079d61c956443f7b9a45`  
		Last Modified: Mon, 15 Jul 2024 19:55:28 GMT  
		Size: 8.1 MB (8098514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71148cb6415c80d9cfbe838ce4441abbd4bb588332346c09bb43c966f302960`  
		Last Modified: Mon, 15 Jul 2024 19:55:28 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240721.0.248532`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:6d743681334a9a3859a1b2633508e2396425085cda41639b1ef35fa74618f9b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:640853c4edb541414067534ad93a86ede65694ffbad88a0dd8cbe3a6eb52491f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271541006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31fe7924ac8c0839a4d426172c2493b6cdf148bfd1c0b519b5bd68923ad7cd64`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20240714.0.246936
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-07-14T00:07:41+00:00
# Sun, 14 Jul 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240714.0.246936' /etc/os-release # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 14 Jul 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c5e7e9ca8c90472562dcd8bbf294446d70a3e2e9a90b7dcffa68a2e4bcc1b0bd`  
		Last Modified: Mon, 15 Jul 2024 19:56:02 GMT  
		Size: 271.5 MB (271531942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c906eceebd38638816e79140e33329ce7fb74b03e0c028433816abcca811829`  
		Last Modified: Mon, 15 Jul 2024 19:55:55 GMT  
		Size: 9.1 KB (9064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:ee56500c52b86e0b9e759bb4a33685197ddd06044760714d875180a749750278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11798888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438ff722dc504d9ccd192b0ca4c4032948dbd34a91877ef90ae7671e8dfc3444`

```dockerfile
```

-	Layers:
	-	`sha256:f386c6d13b5e60d0f8690dd1cb5346cf3681d471f3bbfc137db46f91243ddf6c`  
		Last Modified: Mon, 15 Jul 2024 19:55:56 GMT  
		Size: 11.8 MB (11787385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df627cede0dee729d485e2b522d0f40988f4fbdda91fdedb11616e25775dd2e`  
		Last Modified: Mon, 15 Jul 2024 19:55:55 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240721.0.248532`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:4c53f5cc2575b95b1e93b8dea77b093b2bb95e8d38ca9500b01563de01112d5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:76b4733d4c59cdfcae4a5dced7a6611e8621a502f863631328b362c85ac405c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151081420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071006412c8f62de399d19fafc32bbbfb4df0838e00c098d8bfbeaea3aa6028f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20240714.0.246936
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-07-14T00:07:41+00:00
# Sun, 14 Jul 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240714.0.246936' /etc/os-release # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 14 Jul 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ca363af79b68bf0121632c656d6df30aa97d5a2f1dde5cc230de91515db1bdc1`  
		Last Modified: Mon, 15 Jul 2024 19:55:31 GMT  
		Size: 151.1 MB (151073152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03dd7efb6b9c81c4f2a3560da6bd744bfbf58456182314f5d8ff66925b75e2b`  
		Last Modified: Mon, 15 Jul 2024 19:55:28 GMT  
		Size: 8.3 KB (8268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:6f7b67160aa0c785c38c5e9c5ee1d515e3c2d92ad59efa322d683a083305075b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb8f781d80ef66dbd3646384c2606f28740566d201f5492373b44a2ae06a9a1`

```dockerfile
```

-	Layers:
	-	`sha256:2c3d83448b05a7e33d48f2a52313ffcd4b3c277e9653079d61c956443f7b9a45`  
		Last Modified: Mon, 15 Jul 2024 19:55:28 GMT  
		Size: 8.1 MB (8098514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71148cb6415c80d9cfbe838ce4441abbd4bb588332346c09bb43c966f302960`  
		Last Modified: Mon, 15 Jul 2024 19:55:28 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:f77f1216dccbe2b6bac979ad9d15d8c7bdea1427e819bf0bccf28903b607ac7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0c0119d5d50de6828327a26d5d8456dd2b88b3ff3d73a1d9d01219375220eec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321414198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6d4c7d9ff9c616b20eaf607e77cd232a555a1b09c8fcbbdb50207d13f531e2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20240714.0.246936
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-07-14T00:07:41+00:00
# Sun, 14 Jul 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240714.0.246936' /etc/os-release # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 14 Jul 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:574ead718729478e82012992114b94cd6cd0c20a841ec243e96a2e52d690b52f`  
		Last Modified: Mon, 15 Jul 2024 20:03:08 GMT  
		Size: 321.4 MB (321403991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bda69f104b310390aac9c744b6a53a0051f0fd002f03d3f24b9398ca541dbe`  
		Last Modified: Mon, 15 Jul 2024 20:03:00 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:31983fa9823b2855d7bd067ad82fcfb09090b25978e93c43334878faa5520fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12066311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a400b999aa8af87af952079b49ef1714eba8016ed8b4c14ff6ed2c9acabc30`

```dockerfile
```

-	Layers:
	-	`sha256:742fc773e69ab5230202ee942be7ffe0a0577a26016a229eebcf9b29b4fe3510`  
		Last Modified: Mon, 15 Jul 2024 20:03:01 GMT  
		Size: 12.1 MB (12054751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37a1c1deddca3e59a74a1cc29ffff02cfb5c00be376740f673b7ace798331da`  
		Last Modified: Mon, 15 Jul 2024 20:03:00 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240721.0.248532`

**does not exist** (yet?)
