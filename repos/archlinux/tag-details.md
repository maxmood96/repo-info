<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260222.0.493200`](#archlinuxbase-202602220493200)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260222.0.493200`](#archlinuxbase-devel-202602220493200)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260222.0.493200`](#archlinuxmultilib-devel-202602220493200)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:bb1e5dd58eb79755e736ac530292074f4408572c0fbc4306cd62b431fdf356f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:d1f8276aa44cadeb2e24ddc4cb0d1652adbfa2b1e3666b605d7836b319152d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128244330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16627d83cac7e6bfdc3563c45b4524532f98b883c4d6241654eb19a394fe0dda`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:29 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:32 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:32 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:32 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b59995756522a75a3c4247abc7a41c128cb0ae714bc23abd8d4ea5a6d52f6609`  
		Last Modified: Mon, 23 Feb 2026 19:08:58 GMT  
		Size: 128.2 MB (128235739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371cb576f6bfe6270bc967bcba25fe654f27a04fb479e2cf49e296cd08061b93`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 8.6 KB (8591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:b7b7515da3e20762269219a31b9b459a6c17d12dafa946a6a6e431214cf63381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfb009170c6534b9f71b5867254e29eb7f1c6496c8eadb65c6fbb814c1edf63`

```dockerfile
```

-	Layers:
	-	`sha256:740206aeb7f4cf06ad8019280f6d1f32ad6cb22ab4d0cb6a21c223cfdba8bb51`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 8.5 MB (8477557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4280616b848b7f7acf589a88e0ea0f9f96b1c7f514bff293a4cf4e29f69304e8`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260222.0.493200`

```console
$ docker pull archlinux@sha256:bb1e5dd58eb79755e736ac530292074f4408572c0fbc4306cd62b431fdf356f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260222.0.493200` - linux; amd64

```console
$ docker pull archlinux@sha256:d1f8276aa44cadeb2e24ddc4cb0d1652adbfa2b1e3666b605d7836b319152d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128244330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16627d83cac7e6bfdc3563c45b4524532f98b883c4d6241654eb19a394fe0dda`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:29 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:32 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:32 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:32 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b59995756522a75a3c4247abc7a41c128cb0ae714bc23abd8d4ea5a6d52f6609`  
		Last Modified: Mon, 23 Feb 2026 19:08:58 GMT  
		Size: 128.2 MB (128235739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371cb576f6bfe6270bc967bcba25fe654f27a04fb479e2cf49e296cd08061b93`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 8.6 KB (8591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260222.0.493200` - unknown; unknown

```console
$ docker pull archlinux@sha256:b7b7515da3e20762269219a31b9b459a6c17d12dafa946a6a6e431214cf63381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfb009170c6534b9f71b5867254e29eb7f1c6496c8eadb65c6fbb814c1edf63`

```dockerfile
```

-	Layers:
	-	`sha256:740206aeb7f4cf06ad8019280f6d1f32ad6cb22ab4d0cb6a21c223cfdba8bb51`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 8.5 MB (8477557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4280616b848b7f7acf589a88e0ea0f9f96b1c7f514bff293a4cf4e29f69304e8`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:f7227efe3682a77c6243ac2a1649d3bc93905655a4ddbb540844a3c037ed166e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4de1c037a3250981f3927b888f922a9aed8ff6398233213b71cac2997d588e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245854781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69d5ebd524e60d08a5f7a464fadac8e073606eb860bb26fdf2439bbc5c60086`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:48 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:48 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:48 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f4781d5d587803a33e56cfc1497b8f654f4e958c4748a88bdfed42d8f936fa3`  
		Last Modified: Mon, 23 Feb 2026 19:09:32 GMT  
		Size: 245.8 MB (245845650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9f282a8b5b877ddf817a2013db21d2b5c8c31ec67b8a3e61de3d26f325ebf`  
		Last Modified: Mon, 23 Feb 2026 19:09:27 GMT  
		Size: 9.1 KB (9131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c19ed3c9484fc41a0687c7ef0a2f1531c59ed3396483aba5cd6d8526eb033239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12251627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ddbacc4dc79038f460f4b33777290be965650480569f72d6fe772585bce273`

```dockerfile
```

-	Layers:
	-	`sha256:e167bad5d2e01fe4405279e10a1d5e8a97541ee220e80dcc14fbd4053a180917`  
		Last Modified: Mon, 23 Feb 2026 19:09:28 GMT  
		Size: 12.2 MB (12239916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df4eca89c7d4b5bf89b616ed0c460ba8b60136ffd2f364def51874a811ee332`  
		Last Modified: Mon, 23 Feb 2026 19:09:27 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260222.0.493200`

```console
$ docker pull archlinux@sha256:f7227efe3682a77c6243ac2a1649d3bc93905655a4ddbb540844a3c037ed166e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260222.0.493200` - linux; amd64

```console
$ docker pull archlinux@sha256:4de1c037a3250981f3927b888f922a9aed8ff6398233213b71cac2997d588e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245854781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69d5ebd524e60d08a5f7a464fadac8e073606eb860bb26fdf2439bbc5c60086`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:48 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:48 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:48 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f4781d5d587803a33e56cfc1497b8f654f4e958c4748a88bdfed42d8f936fa3`  
		Last Modified: Mon, 23 Feb 2026 19:09:32 GMT  
		Size: 245.8 MB (245845650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9f282a8b5b877ddf817a2013db21d2b5c8c31ec67b8a3e61de3d26f325ebf`  
		Last Modified: Mon, 23 Feb 2026 19:09:27 GMT  
		Size: 9.1 KB (9131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260222.0.493200` - unknown; unknown

```console
$ docker pull archlinux@sha256:c19ed3c9484fc41a0687c7ef0a2f1531c59ed3396483aba5cd6d8526eb033239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12251627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ddbacc4dc79038f460f4b33777290be965650480569f72d6fe772585bce273`

```dockerfile
```

-	Layers:
	-	`sha256:e167bad5d2e01fe4405279e10a1d5e8a97541ee220e80dcc14fbd4053a180917`  
		Last Modified: Mon, 23 Feb 2026 19:09:28 GMT  
		Size: 12.2 MB (12239916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df4eca89c7d4b5bf89b616ed0c460ba8b60136ffd2f364def51874a811ee332`  
		Last Modified: Mon, 23 Feb 2026 19:09:27 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:bb1e5dd58eb79755e736ac530292074f4408572c0fbc4306cd62b431fdf356f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:d1f8276aa44cadeb2e24ddc4cb0d1652adbfa2b1e3666b605d7836b319152d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128244330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16627d83cac7e6bfdc3563c45b4524532f98b883c4d6241654eb19a394fe0dda`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:29 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:32 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:32 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:32 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b59995756522a75a3c4247abc7a41c128cb0ae714bc23abd8d4ea5a6d52f6609`  
		Last Modified: Mon, 23 Feb 2026 19:08:58 GMT  
		Size: 128.2 MB (128235739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371cb576f6bfe6270bc967bcba25fe654f27a04fb479e2cf49e296cd08061b93`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 8.6 KB (8591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:b7b7515da3e20762269219a31b9b459a6c17d12dafa946a6a6e431214cf63381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfb009170c6534b9f71b5867254e29eb7f1c6496c8eadb65c6fbb814c1edf63`

```dockerfile
```

-	Layers:
	-	`sha256:740206aeb7f4cf06ad8019280f6d1f32ad6cb22ab4d0cb6a21c223cfdba8bb51`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 8.5 MB (8477557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4280616b848b7f7acf589a88e0ea0f9f96b1c7f514bff293a4cf4e29f69304e8`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:04cf8b6ba729ca6b0200cca680f591aed6e8db390ffeec1590e0bd070bad949d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e91594a007d05ac9ec8e154f081de04b27e201c866089e55dd8684976bf21d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268016219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde8eecd7b98b8657c0c1cac0e144a7e7e6bcd5104cf75457cafa5d4a2c46be7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:52 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58cd36eecd001d27b8bf513e4b9a543677be2ff054040e13132e363d7f6654a6`  
		Last Modified: Mon, 23 Feb 2026 19:09:45 GMT  
		Size: 268.0 MB (268005913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b49d38f90bb447f1f7052b78cf5a8ba507a3a6ca6680d285602e0d70812b46`  
		Last Modified: Mon, 23 Feb 2026 19:09:38 GMT  
		Size: 10.3 KB (10306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:104334d3b43f9b92ff91d50d1cfddb594f3bcba0ca1e1fcc1177c8bfd089ac7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12521554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68eddcc66ba3e07caed4f554319ad54e6f86f38dad2bd2abcca7d3af54868db6`

```dockerfile
```

-	Layers:
	-	`sha256:43266162b2b02dbd96e1e6a770fe695a0f5190c367b1fe9bbd0f3142aab724ff`  
		Last Modified: Mon, 23 Feb 2026 19:09:39 GMT  
		Size: 12.5 MB (12509786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0672a7aeed50a24bcf674c64e0f0aa58ea4ef16df0261e810ab3c2bdd75610`  
		Last Modified: Mon, 23 Feb 2026 19:09:38 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260222.0.493200`

```console
$ docker pull archlinux@sha256:04cf8b6ba729ca6b0200cca680f591aed6e8db390ffeec1590e0bd070bad949d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260222.0.493200` - linux; amd64

```console
$ docker pull archlinux@sha256:e91594a007d05ac9ec8e154f081de04b27e201c866089e55dd8684976bf21d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268016219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde8eecd7b98b8657c0c1cac0e144a7e7e6bcd5104cf75457cafa5d4a2c46be7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:46 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:52 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58cd36eecd001d27b8bf513e4b9a543677be2ff054040e13132e363d7f6654a6`  
		Last Modified: Mon, 23 Feb 2026 19:09:45 GMT  
		Size: 268.0 MB (268005913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b49d38f90bb447f1f7052b78cf5a8ba507a3a6ca6680d285602e0d70812b46`  
		Last Modified: Mon, 23 Feb 2026 19:09:38 GMT  
		Size: 10.3 KB (10306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260222.0.493200` - unknown; unknown

```console
$ docker pull archlinux@sha256:104334d3b43f9b92ff91d50d1cfddb594f3bcba0ca1e1fcc1177c8bfd089ac7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12521554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68eddcc66ba3e07caed4f554319ad54e6f86f38dad2bd2abcca7d3af54868db6`

```dockerfile
```

-	Layers:
	-	`sha256:43266162b2b02dbd96e1e6a770fe695a0f5190c367b1fe9bbd0f3142aab724ff`  
		Last Modified: Mon, 23 Feb 2026 19:09:39 GMT  
		Size: 12.5 MB (12509786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0672a7aeed50a24bcf674c64e0f0aa58ea4ef16df0261e810ab3c2bdd75610`  
		Last Modified: Mon, 23 Feb 2026 19:09:38 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
