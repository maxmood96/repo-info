<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241208.0.286830`](#archlinuxbase-202412080286830)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241208.0.286830`](#archlinuxbase-devel-202412080286830)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241208.0.286830`](#archlinuxmultilib-devel-202412080286830)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:ad18112a3888d427b18a004309eff649418b68ddee0e71004c36b87630baac4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:d0c85aec63a57058947faa9bbdcb8365ac31154cb8c5a027156a82ccfa5c0f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151392566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f217f64a9e1cf139b61e10848bd02c1bfb8fb5ba54c3c08c7b7c6fe53b45469`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.version=20241201.0.284684
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.created=2024-12-01T00:07:55+00:00
# Sun, 01 Dec 2024 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241201.0.284684' /etc/os-release # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 01 Dec 2024 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c840bd949e46eea1f5fccc44460b72ca308295126ebc65ec239ec34e806565da`  
		Last Modified: Mon, 02 Dec 2024 20:24:12 GMT  
		Size: 151.4 MB (151384267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a77a916af16c102ae6cf77e9fe94873ae4ea2ff7bff21b47c3fe63468b524a1`  
		Last Modified: Mon, 02 Dec 2024 20:24:10 GMT  
		Size: 8.3 KB (8299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:79cdb4f1a8f6f5005be8c8b9b879b2db1f1d1c54873c81882e7aa4fc560ba8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fea2a22001e23f4fa9182686934abcd3e4c6ab6a590f8c374de0247fce68aa`

```dockerfile
```

-	Layers:
	-	`sha256:ef5e6eb152a51a654837c2aca5140730ab9003e4351ba9a42fa91958a17d3d82`  
		Last Modified: Mon, 02 Dec 2024 20:24:10 GMT  
		Size: 8.1 MB (8082701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e55655663bfb041535ea7ddb2d2d923de6735d187bd0b6ff3210297ea2c8ec4`  
		Last Modified: Mon, 02 Dec 2024 20:24:10 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241208.0.286830`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:39b9ff8523d7f0d652f8b155968e52eba17ffbc8cb9f53c2b810e5b4cd39039c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6c5c0c4a833c46b9b5ddcb482eef88635250f24d012b5939dbcf05549690045c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272518295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cec44a713cc07615d3666d038c0634c4b9a8ed17eae181417b54e69f0e6457c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.version=20241201.0.284684
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.created=2024-12-01T00:07:55+00:00
# Sun, 01 Dec 2024 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241201.0.284684' /etc/os-release # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 01 Dec 2024 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:447fa0c2d9a0915f5b9414e2bc17f366afc9fb0a3280b4e20729471c6b0d7b69`  
		Last Modified: Mon, 02 Dec 2024 20:24:56 GMT  
		Size: 272.5 MB (272509211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f39869530ba41899d092435e7a3512c797f8f92f760d2a5dd1a49409273d55`  
		Last Modified: Mon, 02 Dec 2024 20:24:50 GMT  
		Size: 9.1 KB (9084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0159e907ee9fa393b4c5371177e93d102fe8634799b508f85b7f41ac9cc21795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9527fff2b6a6ac438af00aba56b6fcee8ef8abbf85d80bbc6b46747e2ec868d4`

```dockerfile
```

-	Layers:
	-	`sha256:93058253ef010c77395ffabfa35e0e7e41eb8ea5d8fad30d0c7a4a84fa42e351`  
		Last Modified: Mon, 02 Dec 2024 20:24:51 GMT  
		Size: 11.9 MB (11896380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8eac43fb0af2ddb48c958e7a43ef436174af91884efa80599e28427ff483993`  
		Last Modified: Mon, 02 Dec 2024 20:24:50 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241208.0.286830`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:ad18112a3888d427b18a004309eff649418b68ddee0e71004c36b87630baac4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:d0c85aec63a57058947faa9bbdcb8365ac31154cb8c5a027156a82ccfa5c0f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151392566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f217f64a9e1cf139b61e10848bd02c1bfb8fb5ba54c3c08c7b7c6fe53b45469`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.version=20241201.0.284684
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.created=2024-12-01T00:07:55+00:00
# Sun, 01 Dec 2024 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241201.0.284684' /etc/os-release # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 01 Dec 2024 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c840bd949e46eea1f5fccc44460b72ca308295126ebc65ec239ec34e806565da`  
		Last Modified: Mon, 02 Dec 2024 20:24:12 GMT  
		Size: 151.4 MB (151384267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a77a916af16c102ae6cf77e9fe94873ae4ea2ff7bff21b47c3fe63468b524a1`  
		Last Modified: Mon, 02 Dec 2024 20:24:10 GMT  
		Size: 8.3 KB (8299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:79cdb4f1a8f6f5005be8c8b9b879b2db1f1d1c54873c81882e7aa4fc560ba8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fea2a22001e23f4fa9182686934abcd3e4c6ab6a590f8c374de0247fce68aa`

```dockerfile
```

-	Layers:
	-	`sha256:ef5e6eb152a51a654837c2aca5140730ab9003e4351ba9a42fa91958a17d3d82`  
		Last Modified: Mon, 02 Dec 2024 20:24:10 GMT  
		Size: 8.1 MB (8082701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e55655663bfb041535ea7ddb2d2d923de6735d187bd0b6ff3210297ea2c8ec4`  
		Last Modified: Mon, 02 Dec 2024 20:24:10 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:77812793dd9b43776c5dba213f12b2be2078c835204ef1a91f60d5fb09a8b1cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f2658db6097fb27ecb07d8a3d69352caef97e4df0526fb56b10bffd5e3a966a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322377273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230a73359d2903240dee464607d85d24caae35e7a166be303c5da59d1ce8c0ee`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.version=20241201.0.284684
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.created=2024-12-01T00:07:55+00:00
# Sun, 01 Dec 2024 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241201.0.284684' /etc/os-release # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 01 Dec 2024 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:388a41f6c3933873f2781188065a2fc5a7a89bc7f669b9e9cfcc65845fca3266`  
		Last Modified: Mon, 02 Dec 2024 20:24:48 GMT  
		Size: 322.4 MB (322367076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55adff7b28c71e59b3ccfa5554f730945942a9e64a3da63b7fd9d1f6f37559fa`  
		Last Modified: Mon, 02 Dec 2024 20:24:44 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a5cbe4590ee01c3d3d373b941ee66bfe3ef69ec957064892328cb87a5de80cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11376e310ba181242373c53de127130ecc88cb3050e8425d486f7d4f650a435e`

```dockerfile
```

-	Layers:
	-	`sha256:917b1e23e6e52d622e41a3a44af4daeea162ffd6000866abc2c5ca5b0c57b6d3`  
		Last Modified: Mon, 02 Dec 2024 20:24:44 GMT  
		Size: 12.2 MB (12165176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8e9710b3ee74ed6a73145eecdb933b8e450ffdc6bfce7895b5b4a265848d9da`  
		Last Modified: Mon, 02 Dec 2024 20:24:44 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241208.0.286830`

**does not exist** (yet?)
