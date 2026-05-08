<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260503.0.523481`](#archlinuxbase-202605030523481)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260503.0.523481`](#archlinuxbase-devel-202605030523481)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260503.0.523481`](#archlinuxmultilib-devel-202605030523481)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:5ba8bb318666baef4d33afefc0e65db80f38b23503cb8e7b150d315cc2d4d5da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:52c1b90e0bdffda8bac47c8cf87c5a1883b184fe3513b395f7983559766f9625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129464186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26b5ec8ec89a92d0189a76aa40a864b8c70f9a6feb1353c45b3d85981c3629f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:46:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:46:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1dd624a5d250d23d3790c8017dc38ec1c1abcba105a256f751dd76fefead5bd0`  
		Last Modified: Mon, 20 Apr 2026 21:46:40 GMT  
		Size: 129.5 MB (129455522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ef42a20b3561e23c409877f7f8f4b01e22f927b8755bfc78b5e24a5e9cce5`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:b1a9bba7b891358f6a6351b0d65e578aa9df0229f651cce7f4ae85a1d6b699c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8191391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f512ec2e652487772d147d875364fffeb1c6ed5cc06142df92e2b2d33f387ce7`

```dockerfile
```

-	Layers:
	-	`sha256:e34c7f2f1ce4b7c8f2bd54890f6793e9e45a4676ecf53896dbedfa68c21013f6`  
		Last Modified: Mon, 20 Apr 2026 21:46:38 GMT  
		Size: 8.2 MB (8179463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a766b74985a817edc43640c780b0dccfc7acb8f393cdd2da70f149d1a91cfc06`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260503.0.523481`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:f15064b187aea96308a0252d1eacf514a2ee89aad6d44811f52b733fa9a5e42b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3b828fb58696aab68e5c77350473a332a1746aa44f81a2bc8ad437dce0abb58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247372829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387ed57ebe179807b0f90dd1dafa11a3727c36be26c5355b2f6284fd4d027e18`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:47:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:47:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:47:39 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:47:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c3378b69ab420a6d8805fc88b36f1e41c1f0e83ddf2b2a9e2ff29467b9fa207a`  
		Last Modified: Mon, 20 Apr 2026 21:48:25 GMT  
		Size: 247.4 MB (247363642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad874ddd508cea21e6b14d5038ef0bd201a630e83994d91016b7e5eea408178`  
		Last Modified: Mon, 20 Apr 2026 21:48:17 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:af5cccb41808f62d766c1000aa926fc02a9c19234265172b65f84183a6241d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11993879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1b1b694fec3bee4fe2546cb2ec92355480b15894829b0d683ae6c5f0dd6b42`

```dockerfile
```

-	Layers:
	-	`sha256:af1ba5c2778e02d12f899d96accbb3382acf1d50a41c80162dcdc642db7680c8`  
		Last Modified: Mon, 20 Apr 2026 21:48:17 GMT  
		Size: 12.0 MB (11982168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5300d4d87819feb21d19f2504cbba80a9efc9bf0c8d5d8e5998de4c61c405e6c`  
		Last Modified: Mon, 20 Apr 2026 21:48:17 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260503.0.523481`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:5ba8bb318666baef4d33afefc0e65db80f38b23503cb8e7b150d315cc2d4d5da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:52c1b90e0bdffda8bac47c8cf87c5a1883b184fe3513b395f7983559766f9625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129464186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26b5ec8ec89a92d0189a76aa40a864b8c70f9a6feb1353c45b3d85981c3629f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:46:14 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:46:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:46:16 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:46:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1dd624a5d250d23d3790c8017dc38ec1c1abcba105a256f751dd76fefead5bd0`  
		Last Modified: Mon, 20 Apr 2026 21:46:40 GMT  
		Size: 129.5 MB (129455522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ef42a20b3561e23c409877f7f8f4b01e22f927b8755bfc78b5e24a5e9cce5`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:b1a9bba7b891358f6a6351b0d65e578aa9df0229f651cce7f4ae85a1d6b699c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8191391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f512ec2e652487772d147d875364fffeb1c6ed5cc06142df92e2b2d33f387ce7`

```dockerfile
```

-	Layers:
	-	`sha256:e34c7f2f1ce4b7c8f2bd54890f6793e9e45a4676ecf53896dbedfa68c21013f6`  
		Last Modified: Mon, 20 Apr 2026 21:46:38 GMT  
		Size: 8.2 MB (8179463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a766b74985a817edc43640c780b0dccfc7acb8f393cdd2da70f149d1a91cfc06`  
		Last Modified: Mon, 20 Apr 2026 21:46:37 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:eb1f8b3bd95dcbdbe602bdc85f2166247b7f096b5a646a19aed205bec6771067
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:1aaeb9dff4f60613df76bf30d8899e77d796fa71ab79fcbe76271d565746410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269533467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e355236ea60c3b4ffbbde824611b15a534d57ca69613e7ef05351e5bae5d1a01`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:47:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:47:18 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:47:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:47:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c678628832858cc081c20f7661be106a02b6b75e928d4cdc26418f0a7020ced3`  
		Last Modified: Mon, 20 Apr 2026 21:48:06 GMT  
		Size: 269.5 MB (269523086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168718046a8b227ef0c6c2c79f994f80fdcd4efb19bcaa602417e5eeb3610b02`  
		Last Modified: Mon, 20 Apr 2026 21:47:58 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:e4d2ff284589e4ab1fbbdd9a94de5399b7cd545992b148487995260a5a2ab370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12263806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacb4af6d2fabc230b60eb47dc75a9d119d7ac716b44d900578710af4bb66e41`

```dockerfile
```

-	Layers:
	-	`sha256:bb539de3ec61ed6a39ed5e15cc2c075d24d0006ff38b5762cd5faf0e758a4c62`  
		Last Modified: Mon, 20 Apr 2026 21:47:59 GMT  
		Size: 12.3 MB (12252038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc867a394bf03492bad170a5fc445180ab3e6abd12fbe3513599527d0aa1d06`  
		Last Modified: Mon, 20 Apr 2026 21:47:58 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260503.0.523481`

**does not exist** (yet?)
