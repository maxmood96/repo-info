<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20251221.0.472429`](#archlinuxbase-202512210472429)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20251221.0.472429`](#archlinuxbase-devel-202512210472429)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20251221.0.472429`](#archlinuxmultilib-devel-202512210472429)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:6de1a7bfb793f8d9e24a7d573234f60d011d16db546de5bd777b75707fd4aff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0ad58bc09ac5dc7ecdf43f5c2d221b23400dde42cbf3fb80e78c66046b941687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174702063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ead1ef039fbbda511c65e78867187fd636860f28f730e76f6c4611edd7ee5b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:45:56 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:46:00 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:46:00 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:46:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:20856ddc4ee5b09c44cd703fdcd1da0f57d21ef8caa187e3a10bf779a45f1cf1`  
		Last Modified: Tue, 23 Dec 2025 20:48:33 GMT  
		Size: 174.7 MB (174693399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc1d7f7a8aa5d22544037dd9deddaee9f6566af860631995ff30b6e89b7fffa`  
		Last Modified: Tue, 23 Dec 2025 20:48:23 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:40596493caab5ba46455b9e63e6ed339a00987189e4a7d424ee3d3480d0d7827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5145d5a218381984cac2862be053eef6b15e07d300b53e733676a140ae5065`

```dockerfile
```

-	Layers:
	-	`sha256:4dc37e756cc0d77c2318c75a70348b580ff40f542859cb2618d409e1358941ea`  
		Last Modified: Tue, 23 Dec 2025 20:48:17 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59babf91704b205b12b3453892a2c5823e20aaf34571a6b55478fe031d3fe819`  
		Last Modified: Tue, 23 Dec 2025 20:48:18 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251221.0.472429`

```console
$ docker pull archlinux@sha256:6de1a7bfb793f8d9e24a7d573234f60d011d16db546de5bd777b75707fd4aff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20251221.0.472429` - linux; amd64

```console
$ docker pull archlinux@sha256:0ad58bc09ac5dc7ecdf43f5c2d221b23400dde42cbf3fb80e78c66046b941687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174702063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ead1ef039fbbda511c65e78867187fd636860f28f730e76f6c4611edd7ee5b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:45:56 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:46:00 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:46:00 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:46:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:20856ddc4ee5b09c44cd703fdcd1da0f57d21ef8caa187e3a10bf779a45f1cf1`  
		Last Modified: Tue, 23 Dec 2025 20:48:33 GMT  
		Size: 174.7 MB (174693399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc1d7f7a8aa5d22544037dd9deddaee9f6566af860631995ff30b6e89b7fffa`  
		Last Modified: Tue, 23 Dec 2025 20:48:23 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20251221.0.472429` - unknown; unknown

```console
$ docker pull archlinux@sha256:40596493caab5ba46455b9e63e6ed339a00987189e4a7d424ee3d3480d0d7827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5145d5a218381984cac2862be053eef6b15e07d300b53e733676a140ae5065`

```dockerfile
```

-	Layers:
	-	`sha256:4dc37e756cc0d77c2318c75a70348b580ff40f542859cb2618d409e1358941ea`  
		Last Modified: Tue, 23 Dec 2025 20:48:17 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59babf91704b205b12b3453892a2c5823e20aaf34571a6b55478fe031d3fe819`  
		Last Modified: Tue, 23 Dec 2025 20:48:18 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0a03ad573989e8df9d62ac9d52600a6fb0778016bf5990716a19063e05ebe3c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3a7cfcea321a33e492d28e1ba7faa09c7116fa0b18130b0e313afc6e112db4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292239239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c7c42a0ceccb0d9acbbcde3b86dc975ab88abc0a5a3f636f845eeda15e7992`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:47:14 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:47:21 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:47:21 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:47:21 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:89181a90e29d471acbe88cfa5249d4c5667ae6f755e5b0ee25efa11e859ecd1e`  
		Last Modified: Tue, 23 Dec 2025 20:50:24 GMT  
		Size: 292.2 MB (292230049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a51baa86ca2df506297f2f8b201e37e45d83a13dee8bea2896ef70f3a91b0`  
		Last Modified: Tue, 23 Dec 2025 20:50:10 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8beeca215f557f2c746b24efcf35d95c4ca24ef4e9b6c83ffccf67319fef015b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12157440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cba3e49d6c249b4f7940b31acb8ac22cd5aaf74d1183338616074247b9a1529`

```dockerfile
```

-	Layers:
	-	`sha256:12e3b44f6616703d84d4a038f5da6fcf8b277c544ecd2b9192d383cd5be52b7d`  
		Last Modified: Tue, 23 Dec 2025 20:48:25 GMT  
		Size: 12.1 MB (12145730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0247de5bb34306e5acc92458b0ccea9a310e19bb8ab7fb36cee08dc92b0b3d0`  
		Last Modified: Tue, 23 Dec 2025 20:48:26 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251221.0.472429`

```console
$ docker pull archlinux@sha256:0a03ad573989e8df9d62ac9d52600a6fb0778016bf5990716a19063e05ebe3c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251221.0.472429` - linux; amd64

```console
$ docker pull archlinux@sha256:3a7cfcea321a33e492d28e1ba7faa09c7116fa0b18130b0e313afc6e112db4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292239239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c7c42a0ceccb0d9acbbcde3b86dc975ab88abc0a5a3f636f845eeda15e7992`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:47:14 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:47:21 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:47:21 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:47:21 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:89181a90e29d471acbe88cfa5249d4c5667ae6f755e5b0ee25efa11e859ecd1e`  
		Last Modified: Tue, 23 Dec 2025 20:50:24 GMT  
		Size: 292.2 MB (292230049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a51baa86ca2df506297f2f8b201e37e45d83a13dee8bea2896ef70f3a91b0`  
		Last Modified: Tue, 23 Dec 2025 20:50:10 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251221.0.472429` - unknown; unknown

```console
$ docker pull archlinux@sha256:8beeca215f557f2c746b24efcf35d95c4ca24ef4e9b6c83ffccf67319fef015b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12157440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cba3e49d6c249b4f7940b31acb8ac22cd5aaf74d1183338616074247b9a1529`

```dockerfile
```

-	Layers:
	-	`sha256:12e3b44f6616703d84d4a038f5da6fcf8b277c544ecd2b9192d383cd5be52b7d`  
		Last Modified: Tue, 23 Dec 2025 20:48:25 GMT  
		Size: 12.1 MB (12145730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0247de5bb34306e5acc92458b0ccea9a310e19bb8ab7fb36cee08dc92b0b3d0`  
		Last Modified: Tue, 23 Dec 2025 20:48:26 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:6de1a7bfb793f8d9e24a7d573234f60d011d16db546de5bd777b75707fd4aff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0ad58bc09ac5dc7ecdf43f5c2d221b23400dde42cbf3fb80e78c66046b941687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174702063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ead1ef039fbbda511c65e78867187fd636860f28f730e76f6c4611edd7ee5b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:45:56 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:46:00 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:46:00 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:46:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:20856ddc4ee5b09c44cd703fdcd1da0f57d21ef8caa187e3a10bf779a45f1cf1`  
		Last Modified: Tue, 23 Dec 2025 20:48:33 GMT  
		Size: 174.7 MB (174693399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc1d7f7a8aa5d22544037dd9deddaee9f6566af860631995ff30b6e89b7fffa`  
		Last Modified: Tue, 23 Dec 2025 20:48:23 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:40596493caab5ba46455b9e63e6ed339a00987189e4a7d424ee3d3480d0d7827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5145d5a218381984cac2862be053eef6b15e07d300b53e733676a140ae5065`

```dockerfile
```

-	Layers:
	-	`sha256:4dc37e756cc0d77c2318c75a70348b580ff40f542859cb2618d409e1358941ea`  
		Last Modified: Tue, 23 Dec 2025 20:48:17 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59babf91704b205b12b3453892a2c5823e20aaf34571a6b55478fe031d3fe819`  
		Last Modified: Tue, 23 Dec 2025 20:48:18 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:bc257626b0dde4f463c1631ac8cf32990821f41ed1707ade1a5275c425e058e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:2bf1eff21f22d04c419708e8c6e8fcbe9634e1802e839a80bf60020c540bd138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343559220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b01dbf52d45f4a8f2b53c6e83c820a4b03e614cdec51a1f773f6461924ff51a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:47:07 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:47:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:47:15 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:47:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b3468db2eccc780b7997ac3dd1dd6a1e534bccb26331620aa0e0774b8032bed0`  
		Last Modified: Tue, 23 Dec 2025 20:52:57 GMT  
		Size: 343.5 MB (343548899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95ee9581597d9db3df23bc3583ed8b361f3714d44bbe5b8be5f6e2e3ee1b1fa`  
		Last Modified: Tue, 23 Dec 2025 20:52:48 GMT  
		Size: 10.3 KB (10321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:437274e7fbc426dc350cd3f58365ac6d8c4d3692fd5cc1c633b36599f5d7888d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6793eafa2aafc1ac6fa224df3c13bf04ffb57bd0b537c16ab239a64fbacdffa`

```dockerfile
```

-	Layers:
	-	`sha256:c983f3955a785774649f8afe2305b45c35f25e7ab86766d64d4be759c80909d9`  
		Last Modified: Tue, 23 Dec 2025 20:48:30 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6905de94dcf9e4700c796bc7065d35b5d1f67259fbfb38c83655b1144e320be4`  
		Last Modified: Tue, 23 Dec 2025 20:48:31 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251221.0.472429`

```console
$ docker pull archlinux@sha256:bc257626b0dde4f463c1631ac8cf32990821f41ed1707ade1a5275c425e058e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251221.0.472429` - linux; amd64

```console
$ docker pull archlinux@sha256:2bf1eff21f22d04c419708e8c6e8fcbe9634e1802e839a80bf60020c540bd138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343559220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b01dbf52d45f4a8f2b53c6e83c820a4b03e614cdec51a1f773f6461924ff51a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:47:07 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:47:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:47:15 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:47:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b3468db2eccc780b7997ac3dd1dd6a1e534bccb26331620aa0e0774b8032bed0`  
		Last Modified: Tue, 23 Dec 2025 20:52:57 GMT  
		Size: 343.5 MB (343548899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95ee9581597d9db3df23bc3583ed8b361f3714d44bbe5b8be5f6e2e3ee1b1fa`  
		Last Modified: Tue, 23 Dec 2025 20:52:48 GMT  
		Size: 10.3 KB (10321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251221.0.472429` - unknown; unknown

```console
$ docker pull archlinux@sha256:437274e7fbc426dc350cd3f58365ac6d8c4d3692fd5cc1c633b36599f5d7888d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6793eafa2aafc1ac6fa224df3c13bf04ffb57bd0b537c16ab239a64fbacdffa`

```dockerfile
```

-	Layers:
	-	`sha256:c983f3955a785774649f8afe2305b45c35f25e7ab86766d64d4be759c80909d9`  
		Last Modified: Tue, 23 Dec 2025 20:48:30 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6905de94dcf9e4700c796bc7065d35b5d1f67259fbfb38c83655b1144e320be4`  
		Last Modified: Tue, 23 Dec 2025 20:48:31 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
