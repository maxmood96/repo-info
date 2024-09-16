<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240915.0.262934`](#archlinuxbase-202409150262934)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240915.0.262934`](#archlinuxbase-devel-202409150262934)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240915.0.262934`](#archlinuxmultilib-devel-202409150262934)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:dbcf6a01a24a56c96b179d40f2425fd257f58e6ff8c5c54c1aa66251442d6f80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a10e51dd0694d6c4142754e9d06cbce7baf91ace8031a30df37064d1091ab414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151275787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e34eb59b71012351582a045b4fff0f634e7419658a7110e2f83fe92a1c9c9a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.version=20240908.0.261281
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.created=2024-09-08T00:07:27+00:00
# Sun, 08 Sep 2024 00:07:27 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240908.0.261281' /etc/os-release # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 00:07:27 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:48c737288e6ef23c01fa5e142b7634c1350a21e5861dc935a45de8c004fb10ed`  
		Last Modified: Mon, 09 Sep 2024 19:04:38 GMT  
		Size: 151.3 MB (151267511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98025c0a629bee7f87f0a8a61dfa36c301f809d98d57997906d7e99b1b8a88`  
		Last Modified: Mon, 09 Sep 2024 19:04:34 GMT  
		Size: 8.3 KB (8276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:bd57c1bbb7e09e2ff312b49d6c4d6dde2fd55ab4077ca82c936dac32ed1084c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66e83baba40b005da4c04d9de63bbacb625fc60c71b9ce9fc9b6c35df1eeae6`

```dockerfile
```

-	Layers:
	-	`sha256:f60d3ae488e9d9793aa105257d6b52d31de4588a33c852c42f0d70b3f283aaf2`  
		Last Modified: Mon, 09 Sep 2024 19:04:35 GMT  
		Size: 8.1 MB (8103997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35492009cbb34845e893e537fb1729615d7daa4a5c1d0b3ef47b21796b85204`  
		Last Modified: Mon, 09 Sep 2024 19:04:34 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240915.0.262934`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:82d29f4616cbe45e42887f0369dceea6b67768e8ac99c925155e47d1ed3c82cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:a882417f30e2193e42078ab847fccaadc88ffb77b10bd2363d27cd913bc6c869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272290652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82180bf4d936f57230c788e5b2a3049aeb2fbee773da3e63751e9e6cacf9c00a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.version=20240908.0.261281
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.created=2024-09-08T00:07:27+00:00
# Sun, 08 Sep 2024 00:07:27 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240908.0.261281' /etc/os-release # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 00:07:27 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b036fa806bbbda498e1d11af9ea2e9f0da818b514273180d0d800a03cb9b15d8`  
		Last Modified: Mon, 09 Sep 2024 19:04:53 GMT  
		Size: 272.3 MB (272281606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27595973d89a3e1e051da627231a077d3a8863053b980857795e0dcaf478ad2a`  
		Last Modified: Mon, 09 Sep 2024 19:04:49 GMT  
		Size: 9.0 KB (9046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:633bdf2e7bb1670387d4bb8d207a0d204c1046bcf0d12fd308195d6ce4eda44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11913861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dece966292a85e07badf559ea4efcf80af377088af670107d0388a57193115`

```dockerfile
```

-	Layers:
	-	`sha256:b38e4c18f5d27aa9536c9506fdad1abc41e66fddd82d022e51495d28be2f5273`  
		Last Modified: Mon, 09 Sep 2024 19:04:50 GMT  
		Size: 11.9 MB (11902358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8659b2b8584b1743849eaf36973b789ea3a77d0b7871899ee06d17eb9c96a9`  
		Last Modified: Mon, 09 Sep 2024 19:04:50 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240915.0.262934`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:dbcf6a01a24a56c96b179d40f2425fd257f58e6ff8c5c54c1aa66251442d6f80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:a10e51dd0694d6c4142754e9d06cbce7baf91ace8031a30df37064d1091ab414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151275787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e34eb59b71012351582a045b4fff0f634e7419658a7110e2f83fe92a1c9c9a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.version=20240908.0.261281
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.created=2024-09-08T00:07:27+00:00
# Sun, 08 Sep 2024 00:07:27 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240908.0.261281' /etc/os-release # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 00:07:27 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:48c737288e6ef23c01fa5e142b7634c1350a21e5861dc935a45de8c004fb10ed`  
		Last Modified: Mon, 09 Sep 2024 19:04:38 GMT  
		Size: 151.3 MB (151267511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98025c0a629bee7f87f0a8a61dfa36c301f809d98d57997906d7e99b1b8a88`  
		Last Modified: Mon, 09 Sep 2024 19:04:34 GMT  
		Size: 8.3 KB (8276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:bd57c1bbb7e09e2ff312b49d6c4d6dde2fd55ab4077ca82c936dac32ed1084c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66e83baba40b005da4c04d9de63bbacb625fc60c71b9ce9fc9b6c35df1eeae6`

```dockerfile
```

-	Layers:
	-	`sha256:f60d3ae488e9d9793aa105257d6b52d31de4588a33c852c42f0d70b3f283aaf2`  
		Last Modified: Mon, 09 Sep 2024 19:04:35 GMT  
		Size: 8.1 MB (8103997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35492009cbb34845e893e537fb1729615d7daa4a5c1d0b3ef47b21796b85204`  
		Last Modified: Mon, 09 Sep 2024 19:04:34 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:34476c1e210f7c0de33d33569fa636da564751c79fb0d6cf59374e84aebed268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8c7f0e4ed679bbc66e3b5b78dc876a65a02ca319702d022164a4e22dcdc063da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322164261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad11b0d9aec60b3ff4eeeafdf71d06f31260b896a1d5c1ff11f913ba8e6b461`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.version=20240908.0.261281
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.created=2024-09-08T00:07:27+00:00
# Sun, 08 Sep 2024 00:07:27 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240908.0.261281' /etc/os-release # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 00:07:27 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53ae51d027274ad9e04c1b0f683a81d643a09ad9b3892ccade4d40f11ed81097`  
		Last Modified: Mon, 09 Sep 2024 19:05:05 GMT  
		Size: 322.2 MB (322154051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae698b60132ac648a39a026af430e8c78450761b5087a57cedfaebffeaa9673`  
		Last Modified: Mon, 09 Sep 2024 19:05:00 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:250f99d3f1bbc14786d024914ed1afe9f0ffe1ff5aa396f1b3389366817cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12181257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1574ef952546a8886fd2a699d768e2c7303577a4312fedd672a997153e2a38`

```dockerfile
```

-	Layers:
	-	`sha256:b8f31e5d5209e48f38c957405a5b2fe7abd312372d22fed2950fa41fec45938f`  
		Last Modified: Mon, 09 Sep 2024 19:05:00 GMT  
		Size: 12.2 MB (12169697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2bdb9a743029eb08939a6c7c64af51e8cc9b0f85425604208bc4185ab08594b`  
		Last Modified: Mon, 09 Sep 2024 19:05:00 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240915.0.262934`

**does not exist** (yet?)
