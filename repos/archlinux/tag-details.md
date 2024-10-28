<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241027.0.273886`](#archlinuxbase-202410270273886)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241027.0.273886`](#archlinuxbase-devel-202410270273886)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241027.0.273886`](#archlinuxmultilib-devel-202410270273886)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:3fb8e79e4037db1536d331dba905e234fa18c8206191458a927013a2d2dafc50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:aa503a37fe694372fc3604121a796912641f222f14b1225de5ddd0eb02b59fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151203151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e1b7cf5154015ecb82ca0bdd1bbb9bde38513a399bf5f33f604b8336dee359`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20241020.0.271562
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-10-20T00:07:52+00:00
# Sun, 20 Oct 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241020.0.271562' /etc/os-release # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 20 Oct 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6de47c16693df274d55e255de3d91c694837a0b7239c6c53046de67bcad64de7`  
		Last Modified: Mon, 21 Oct 2024 17:57:37 GMT  
		Size: 151.2 MB (151194931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864e0e7bea0968d13d08d3a04a8a182a58155b86723b988efa20e29846d0480`  
		Last Modified: Mon, 21 Oct 2024 17:57:30 GMT  
		Size: 8.2 KB (8220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:a116f4fd9320641bc7f3154209adcd78bf8008c3f635ec7f56c57dd8dfb10527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8151541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2748bc660c0f89edd9f6fccc01062d52426b5262d70cd2ca42b4a7ec2798b375`

```dockerfile
```

-	Layers:
	-	`sha256:90e4e5a161049541897a14973dc0464055b2db355f06dafd02f19ca8f961281c`  
		Last Modified: Mon, 21 Oct 2024 17:57:30 GMT  
		Size: 8.1 MB (8139787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ddc564fd6a1b2c1341250ab7a83b668cb21340aa185faf8ad4a473b162cadb`  
		Last Modified: Mon, 21 Oct 2024 17:57:30 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241027.0.273886`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:f493b023ea4e1dbc4073bf9f39898dfa153286f47547d1a5f886105e66557e5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:bc750120ea9ea5b5f99248fe3cd9b22f85551883c0b1f4d3e59cd23c60791aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272210183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c7f3c47df3e45b4a24087b01b8b13cadfce0b5bf4870397dec0270c5c27cc4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20241020.0.271562
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-10-20T00:07:52+00:00
# Sun, 20 Oct 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241020.0.271562' /etc/os-release # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 20 Oct 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:024e1215271164d7d8737dba631eaddb352b7bc965fb72669caed0e2e11e8691`  
		Last Modified: Mon, 21 Oct 2024 17:58:02 GMT  
		Size: 272.2 MB (272201158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4b88dd35c8937bcdda7d80a9ab0469d311f86f0910403ce62f7f0996cfa96d`  
		Last Modified: Mon, 21 Oct 2024 17:57:58 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2099e7a9707bcdb7878c12b702c1ed3cff50026bc0aa5676ef4bd7d655370faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11957777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1584024742a905811323458f439fada2b4d0930b6c8f165f6b600be764e4ea84`

```dockerfile
```

-	Layers:
	-	`sha256:ba438d409d2d69beae59e756762cb69d164bd42ab3be2467b1c9542e8825fdef`  
		Last Modified: Mon, 21 Oct 2024 17:57:58 GMT  
		Size: 11.9 MB (11946240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18b546c38a04a8de21d0b9c536c80920f3a94e18db166f148fa91f3a7c84d10`  
		Last Modified: Mon, 21 Oct 2024 17:57:58 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241027.0.273886`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:3fb8e79e4037db1536d331dba905e234fa18c8206191458a927013a2d2dafc50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:aa503a37fe694372fc3604121a796912641f222f14b1225de5ddd0eb02b59fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151203151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e1b7cf5154015ecb82ca0bdd1bbb9bde38513a399bf5f33f604b8336dee359`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20241020.0.271562
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-10-20T00:07:52+00:00
# Sun, 20 Oct 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241020.0.271562' /etc/os-release # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 20 Oct 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6de47c16693df274d55e255de3d91c694837a0b7239c6c53046de67bcad64de7`  
		Last Modified: Mon, 21 Oct 2024 17:57:37 GMT  
		Size: 151.2 MB (151194931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864e0e7bea0968d13d08d3a04a8a182a58155b86723b988efa20e29846d0480`  
		Last Modified: Mon, 21 Oct 2024 17:57:30 GMT  
		Size: 8.2 KB (8220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:a116f4fd9320641bc7f3154209adcd78bf8008c3f635ec7f56c57dd8dfb10527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8151541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2748bc660c0f89edd9f6fccc01062d52426b5262d70cd2ca42b4a7ec2798b375`

```dockerfile
```

-	Layers:
	-	`sha256:90e4e5a161049541897a14973dc0464055b2db355f06dafd02f19ca8f961281c`  
		Last Modified: Mon, 21 Oct 2024 17:57:30 GMT  
		Size: 8.1 MB (8139787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ddc564fd6a1b2c1341250ab7a83b668cb21340aa185faf8ad4a473b162cadb`  
		Last Modified: Mon, 21 Oct 2024 17:57:30 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:2a6d6172047c9b6c27f772a91500717c0eddff4cceabe8f0791c4387745efb93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7a87aef720d50d76e8d40edb4d1cc65f3ddeca86d0aaabd877b8390e751f33a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322058840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b097299855429aa5de6b4381218c344872399c99e54cf495e32f89b3dbc954e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20241020.0.271562
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-10-20T00:07:52+00:00
# Sun, 20 Oct 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241020.0.271562' /etc/os-release # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 20 Oct 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:fddc4115830b94cf3617c5c01934353eff594fc95ce15d3ab01cf59987bbaeaa`  
		Last Modified: Mon, 21 Oct 2024 17:58:09 GMT  
		Size: 322.0 MB (322048722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca489cfbc6b5c3f92d35d06d6c9dda00cb6e5283e4a23767e4ed388f980345b4`  
		Last Modified: Mon, 21 Oct 2024 17:58:05 GMT  
		Size: 10.1 KB (10118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:7a26696b80cbb6f623b8eb0ea368556c353d2fa70ff8041e13c03584a0d9a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12226630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6150a8e7914c52f2df86036903fb680c84c4cbee55df4a5d3b8a1481796df5`

```dockerfile
```

-	Layers:
	-	`sha256:58399ad9e575fb269b2d56c39f95f8765be1123fb83551015fda7bcaf24a09f7`  
		Last Modified: Mon, 21 Oct 2024 17:58:05 GMT  
		Size: 12.2 MB (12215036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15139c3ed67f1cec28146bd2425a4cde791a88b11f432cac6d34b60fab53fd4a`  
		Last Modified: Mon, 21 Oct 2024 17:58:05 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241027.0.273886`

**does not exist** (yet?)
