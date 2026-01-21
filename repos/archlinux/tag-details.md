<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260118.0.482696`](#archlinuxbase-202601180482696)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260118.0.482696`](#archlinuxbase-devel-202601180482696)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260118.0.482696`](#archlinuxmultilib-devel-202601180482696)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:f5add4183c5f05abf3b65489447aee6d5714db735cd639d4000505a59838e1c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:04c1c7e8d23f22bfd227e4d683fe0eb456a9dfc5bc1c312de750b7ae720cdd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176210607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686070b1d07a5fd94e0a4b7e47d71aa36294d8eb3a15db0e1a81a8ac2c983850`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:24:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:24:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:24:55 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:24:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:43b8931ca17a7cee66b4fc84f9abf7f738aa10952d5655e4981afc121d7ada16`  
		Last Modified: Tue, 20 Jan 2026 19:32:00 GMT  
		Size: 176.2 MB (176201833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8361e5378b827e04240b486140666179acdc50001735e54f5d5568817d7e34e2`  
		Last Modified: Tue, 20 Jan 2026 17:25:24 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:9588e463d1f90e50c520be4fb672ec465fba2b034be8647d9f02bc5428ed4141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f32dff9d3c9f73978b3694683ed14d9ea82cbb918aaef34bed8a6768f7be669`

```dockerfile
```

-	Layers:
	-	`sha256:e9862745047189b732b0272e03bf98c4cbd8cca1725a0350cd392415d926182a`  
		Last Modified: Tue, 20 Jan 2026 20:48:18 GMT  
		Size: 8.4 MB (8398787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea89aeea5b14acc01e42497b38ecb55d77a86bca4f137c6b0adcd053e2ec7c9`  
		Last Modified: Tue, 20 Jan 2026 17:25:24 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260118.0.482696`

```console
$ docker pull archlinux@sha256:f5add4183c5f05abf3b65489447aee6d5714db735cd639d4000505a59838e1c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260118.0.482696` - linux; amd64

```console
$ docker pull archlinux@sha256:04c1c7e8d23f22bfd227e4d683fe0eb456a9dfc5bc1c312de750b7ae720cdd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176210607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686070b1d07a5fd94e0a4b7e47d71aa36294d8eb3a15db0e1a81a8ac2c983850`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:24:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:24:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:24:55 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:24:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:43b8931ca17a7cee66b4fc84f9abf7f738aa10952d5655e4981afc121d7ada16`  
		Last Modified: Tue, 20 Jan 2026 19:32:00 GMT  
		Size: 176.2 MB (176201833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8361e5378b827e04240b486140666179acdc50001735e54f5d5568817d7e34e2`  
		Last Modified: Tue, 20 Jan 2026 17:25:24 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260118.0.482696` - unknown; unknown

```console
$ docker pull archlinux@sha256:9588e463d1f90e50c520be4fb672ec465fba2b034be8647d9f02bc5428ed4141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f32dff9d3c9f73978b3694683ed14d9ea82cbb918aaef34bed8a6768f7be669`

```dockerfile
```

-	Layers:
	-	`sha256:e9862745047189b732b0272e03bf98c4cbd8cca1725a0350cd392415d926182a`  
		Last Modified: Tue, 20 Jan 2026 20:48:18 GMT  
		Size: 8.4 MB (8398787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea89aeea5b14acc01e42497b38ecb55d77a86bca4f137c6b0adcd053e2ec7c9`  
		Last Modified: Tue, 20 Jan 2026 17:25:24 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:d2bd09bd30dc1199ba6f35bc575292957a4a24377fb137d0f999817bc29adc17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:54635d6ebf2fd2b0e61f53550764e4e23b9ec5cfb3461405e2ee91a3181c0a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293739464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f912e82db9a80c6e81598df987caccc156e03351f1a9a1455f6f3291700697`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:26:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:26:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:26:10 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:26:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1824341832c208f8b5ba9f73dd22bb8fa28ca60dfce33b1abdf6eafd18c27adb`  
		Last Modified: Tue, 20 Jan 2026 20:48:31 GMT  
		Size: 293.7 MB (293730101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da34fdd0475f9731bef22d34dce153980aedf456f92bc1a9d30819c789a732b0`  
		Last Modified: Tue, 20 Jan 2026 17:27:28 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:705af7fe0b24fedc32e39bed3783793b010e14df70da5dfbb3fc56c1130c8ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b859631d3430bb2d1a4541e9fd7b3e1f9dba67547de638f226bdfcd3726b2c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ec821b643c5be5385d65d19ebfc9d735fa7568b65d08b6d55466f7bfe29610a`  
		Last Modified: Tue, 20 Jan 2026 20:48:23 GMT  
		Size: 12.2 MB (12161122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3356d37d4f7a290ab5e1f719bf29e9ad20d76500f7adc8dc11574f0cf5779cb9`  
		Last Modified: Tue, 20 Jan 2026 20:48:24 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260118.0.482696`

```console
$ docker pull archlinux@sha256:d2bd09bd30dc1199ba6f35bc575292957a4a24377fb137d0f999817bc29adc17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260118.0.482696` - linux; amd64

```console
$ docker pull archlinux@sha256:54635d6ebf2fd2b0e61f53550764e4e23b9ec5cfb3461405e2ee91a3181c0a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293739464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f912e82db9a80c6e81598df987caccc156e03351f1a9a1455f6f3291700697`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:26:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:26:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:26:10 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:26:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1824341832c208f8b5ba9f73dd22bb8fa28ca60dfce33b1abdf6eafd18c27adb`  
		Last Modified: Tue, 20 Jan 2026 20:48:31 GMT  
		Size: 293.7 MB (293730101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da34fdd0475f9731bef22d34dce153980aedf456f92bc1a9d30819c789a732b0`  
		Last Modified: Tue, 20 Jan 2026 17:27:28 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260118.0.482696` - unknown; unknown

```console
$ docker pull archlinux@sha256:705af7fe0b24fedc32e39bed3783793b010e14df70da5dfbb3fc56c1130c8ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b859631d3430bb2d1a4541e9fd7b3e1f9dba67547de638f226bdfcd3726b2c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ec821b643c5be5385d65d19ebfc9d735fa7568b65d08b6d55466f7bfe29610a`  
		Last Modified: Tue, 20 Jan 2026 20:48:23 GMT  
		Size: 12.2 MB (12161122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3356d37d4f7a290ab5e1f719bf29e9ad20d76500f7adc8dc11574f0cf5779cb9`  
		Last Modified: Tue, 20 Jan 2026 20:48:24 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:f5add4183c5f05abf3b65489447aee6d5714db735cd639d4000505a59838e1c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:04c1c7e8d23f22bfd227e4d683fe0eb456a9dfc5bc1c312de750b7ae720cdd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176210607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686070b1d07a5fd94e0a4b7e47d71aa36294d8eb3a15db0e1a81a8ac2c983850`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:24:52 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:24:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:24:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:24:55 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:24:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:43b8931ca17a7cee66b4fc84f9abf7f738aa10952d5655e4981afc121d7ada16`  
		Last Modified: Tue, 20 Jan 2026 19:32:00 GMT  
		Size: 176.2 MB (176201833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8361e5378b827e04240b486140666179acdc50001735e54f5d5568817d7e34e2`  
		Last Modified: Tue, 20 Jan 2026 17:25:24 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:9588e463d1f90e50c520be4fb672ec465fba2b034be8647d9f02bc5428ed4141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f32dff9d3c9f73978b3694683ed14d9ea82cbb918aaef34bed8a6768f7be669`

```dockerfile
```

-	Layers:
	-	`sha256:e9862745047189b732b0272e03bf98c4cbd8cca1725a0350cd392415d926182a`  
		Last Modified: Tue, 20 Jan 2026 20:48:18 GMT  
		Size: 8.4 MB (8398787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea89aeea5b14acc01e42497b38ecb55d77a86bca4f137c6b0adcd053e2ec7c9`  
		Last Modified: Tue, 20 Jan 2026 17:25:24 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:19dcebdda856065d0384ab74ffa96eccb3d28cd789bc447c8226d19a4733d77c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:cc333cb344d8cb4915cb167b31480a0879303a790b555a64051dd40335669222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345062239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07513cb60684845d860b4812ff47411ab2131ed890f511fc33b3ae4f7aa765f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:26:09 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:26:17 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:26:17 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:26:17 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9126e44ff2b632f68545a4b591fcdbfe6b0a5eb414c823621ffaa0e64e15b4b`  
		Last Modified: Tue, 20 Jan 2026 17:28:35 GMT  
		Size: 345.1 MB (345051773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4aba7bbe4bf25681eae44175c0000ca519f34e75e60d9021846669d1f7d734a`  
		Last Modified: Tue, 20 Jan 2026 17:27:37 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bd4a94bc0c5d6e2c236d55727237144ca65376741502d2745451292d0f0e125f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12441683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46a63af9c62ba5b321040095a7cd86ea17a15a0526d50074365189f79ae731a`

```dockerfile
```

-	Layers:
	-	`sha256:60d19c113113aff0c089def5af1cdcdc8def6211c154e4d64cbf4efeb20b9e8b`  
		Last Modified: Tue, 20 Jan 2026 17:27:11 GMT  
		Size: 12.4 MB (12429915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f1b5635cfb41faeb7e5a11c7a7bc99cab8b3e5406afd89e2216bd002752b74`  
		Last Modified: Tue, 20 Jan 2026 17:27:10 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260118.0.482696`

```console
$ docker pull archlinux@sha256:19dcebdda856065d0384ab74ffa96eccb3d28cd789bc447c8226d19a4733d77c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260118.0.482696` - linux; amd64

```console
$ docker pull archlinux@sha256:cc333cb344d8cb4915cb167b31480a0879303a790b555a64051dd40335669222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345062239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07513cb60684845d860b4812ff47411ab2131ed890f511fc33b3ae4f7aa765f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:26:09 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:26:17 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:26:17 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:26:17 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9126e44ff2b632f68545a4b591fcdbfe6b0a5eb414c823621ffaa0e64e15b4b`  
		Last Modified: Tue, 20 Jan 2026 17:28:35 GMT  
		Size: 345.1 MB (345051773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4aba7bbe4bf25681eae44175c0000ca519f34e75e60d9021846669d1f7d734a`  
		Last Modified: Tue, 20 Jan 2026 17:27:37 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260118.0.482696` - unknown; unknown

```console
$ docker pull archlinux@sha256:bd4a94bc0c5d6e2c236d55727237144ca65376741502d2745451292d0f0e125f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12441683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46a63af9c62ba5b321040095a7cd86ea17a15a0526d50074365189f79ae731a`

```dockerfile
```

-	Layers:
	-	`sha256:60d19c113113aff0c089def5af1cdcdc8def6211c154e4d64cbf4efeb20b9e8b`  
		Last Modified: Tue, 20 Jan 2026 17:27:11 GMT  
		Size: 12.4 MB (12429915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f1b5635cfb41faeb7e5a11c7a7bc99cab8b3e5406afd89e2216bd002752b74`  
		Last Modified: Tue, 20 Jan 2026 17:27:10 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
