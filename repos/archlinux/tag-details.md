<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260412.0.513370`](#archlinuxbase-202604120513370)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260412.0.513370`](#archlinuxbase-devel-202604120513370)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260412.0.513370`](#archlinuxmultilib-devel-202604120513370)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:b4df475619469581537637ceaace6075f4912ea1cd6db6b99d463e3a72969d04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:bada17b14eeb70c3926e67951ac95291548c25a4b4c83b73c846838e5e292700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128815340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0861fbb9176ee3054b4213768d899fcaa75ed245638766f323fa8f8a81d439b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.version=20260405.0.511327
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.created=2026-04-05T00:07:03+00:00
# Mon, 06 Apr 2026 18:07:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 06 Apr 2026 18:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260405.0.511327' /etc/os-release # buildkit
# Mon, 06 Apr 2026 18:07:42 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9ea86d6f9b5d6505c95a0472fee5fc3797e6b14e31f3f8d9907664194475576`  
		Last Modified: Mon, 06 Apr 2026 18:08:08 GMT  
		Size: 128.8 MB (128806757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd69c77b3164c13f3b81ca340f9329fe8cd6ab2d5b0a767ed9438c9ce57e086`  
		Last Modified: Mon, 06 Apr 2026 18:08:04 GMT  
		Size: 8.6 KB (8583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:1429e29b3e97f6373434a9ce20d6378dbe0aa43e0f7d4b7f6f70d011ce6e3717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8161782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775bda38ab896d13059ff45727e36db3eb165c71145e061ce32cbcab69390baa`

```dockerfile
```

-	Layers:
	-	`sha256:9393903773d2b6d03edb153adeeb133754d305ec85b78da2d4fcf12cee9c9914`  
		Last Modified: Mon, 06 Apr 2026 18:08:05 GMT  
		Size: 8.1 MB (8149853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8956b74e0052461ee4aa05135480c83f001d32562eb5be820af55c3e1b6be179`  
		Last Modified: Mon, 06 Apr 2026 18:08:05 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260412.0.513370`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:4a48384d9725d1901fca133f43b6a41dee98acee2c9379c4b4d81bed77051cdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e1b8968819709959fec2cd9115822300e1ae9e4ab436234445fe6229a7ce0677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246478432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7f571c205bee9bfa5e886814f50a918a626847aafa9ba3a7db8443542f3e00`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.version=20260405.0.511327
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.created=2026-04-05T00:07:03+00:00
# Mon, 06 Apr 2026 18:07:51 GMT
COPY /rootfs/ / # buildkit
# Mon, 06 Apr 2026 18:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260405.0.511327' /etc/os-release # buildkit
# Mon, 06 Apr 2026 18:07:56 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:009772841e8246ba72583eea022399749cacc094fee5279ea7e29f66196abc27`  
		Last Modified: Mon, 06 Apr 2026 18:08:40 GMT  
		Size: 246.5 MB (246469311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea00216238e42ffc58161f8b6ab72ce4e2805ffbe72fbe0cdd1f52137530b764`  
		Last Modified: Mon, 06 Apr 2026 18:08:34 GMT  
		Size: 9.1 KB (9121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0d05689f7bbe1df2c8784ff215e3d7357e07ea158d6e9f383b3a787fedeebac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11946412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd758ae78da41d848bff8569a7bfe6b8987a42b7ddcd1b748c6465f59ce4dc7`

```dockerfile
```

-	Layers:
	-	`sha256:4fde26159ffe8a2c5bf51ba8f5aa0d7d7b404db30ec7b4ccd2d1b7b3cd471e5d`  
		Last Modified: Mon, 06 Apr 2026 18:08:35 GMT  
		Size: 11.9 MB (11934701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc852de4f7a8d5b5d7a64bb46cba0934679e404a0c8955c6614b380b03d85521`  
		Last Modified: Mon, 06 Apr 2026 18:08:34 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260412.0.513370`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:b4df475619469581537637ceaace6075f4912ea1cd6db6b99d463e3a72969d04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:bada17b14eeb70c3926e67951ac95291548c25a4b4c83b73c846838e5e292700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128815340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0861fbb9176ee3054b4213768d899fcaa75ed245638766f323fa8f8a81d439b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.version=20260405.0.511327
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.created=2026-04-05T00:07:03+00:00
# Mon, 06 Apr 2026 18:07:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 06 Apr 2026 18:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260405.0.511327' /etc/os-release # buildkit
# Mon, 06 Apr 2026 18:07:42 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9ea86d6f9b5d6505c95a0472fee5fc3797e6b14e31f3f8d9907664194475576`  
		Last Modified: Mon, 06 Apr 2026 18:08:08 GMT  
		Size: 128.8 MB (128806757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd69c77b3164c13f3b81ca340f9329fe8cd6ab2d5b0a767ed9438c9ce57e086`  
		Last Modified: Mon, 06 Apr 2026 18:08:04 GMT  
		Size: 8.6 KB (8583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:1429e29b3e97f6373434a9ce20d6378dbe0aa43e0f7d4b7f6f70d011ce6e3717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8161782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775bda38ab896d13059ff45727e36db3eb165c71145e061ce32cbcab69390baa`

```dockerfile
```

-	Layers:
	-	`sha256:9393903773d2b6d03edb153adeeb133754d305ec85b78da2d4fcf12cee9c9914`  
		Last Modified: Mon, 06 Apr 2026 18:08:05 GMT  
		Size: 8.1 MB (8149853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8956b74e0052461ee4aa05135480c83f001d32562eb5be820af55c3e1b6be179`  
		Last Modified: Mon, 06 Apr 2026 18:08:05 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:f02e8deedf73c48aa71ce29c8ae4de5f681991125ef6c627d4eef9e657a3507a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4a8aa2fad48d940a0084f4c99cc0b92484e0d9b18d722afe74add42ff5491754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268641078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f817144db725d1c67e2d186a6b80a74fc3381a29148257dc3a1683b7ea284`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.version=20260405.0.511327
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.created=2026-04-05T00:07:03+00:00
# Mon, 06 Apr 2026 18:07:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 06 Apr 2026 18:08:03 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260405.0.511327' /etc/os-release # buildkit
# Mon, 06 Apr 2026 18:08:03 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:08:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:68571b5330036f5d6913e7b3579ec3358f381968b99a3cee984742027bcea8ed`  
		Last Modified: Mon, 06 Apr 2026 18:08:55 GMT  
		Size: 268.6 MB (268630768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8802103e1d0f4f426aed3656c2ad0fa433dda130f7351925ff64d09fe40cfb`  
		Last Modified: Mon, 06 Apr 2026 18:08:48 GMT  
		Size: 10.3 KB (10310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:82ee2d0174b6984698b05db4aa49f0e78216aae8e618c7ce8775d619c2a115f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12216339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9029ad14072fb30ca7ba99c46fb5f89de23d9374d760be00f657fdf22337aa3`

```dockerfile
```

-	Layers:
	-	`sha256:020b6df1b2b0428d27b8f9f7f0492bc1ccbfb4e77d23ed9d774cc56adfcb54b5`  
		Last Modified: Mon, 06 Apr 2026 18:08:48 GMT  
		Size: 12.2 MB (12204571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7748bae67c70dea5f06af7977d6da537c679483418da19dafb7c78bf90a0a0fa`  
		Last Modified: Mon, 06 Apr 2026 18:08:47 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260412.0.513370`

**does not exist** (yet?)
