<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250706.0.377547`](#archlinuxbase-202507060377547)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250706.0.377547`](#archlinuxbase-devel-202507060377547)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250706.0.377547`](#archlinuxmultilib-devel-202507060377547)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:7ca06cad29fe509ea1b4a0fb40485ca410fe5fdbea39888c5f3169b4961b2b14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9c1cd902a49c2fa899622c286cba954f82b95b00abc1d9e094103eed3600594a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163274141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac8e88fb26b28530e3448585327a70fe5d414f5af5f91c60a455dfd1042338`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e4655ef3515a3583f60522ea0db589115ae05d3ea8243775d40be9fd671a514a`  
		Last Modified: Mon, 07 Jul 2025 22:48:31 GMT  
		Size: 163.3 MB (163265783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7df37c7b4083f7f8c7c1ed77b16aa0f7e02318ac65fa5a6ce1a136eed4439`  
		Last Modified: Mon, 07 Jul 2025 20:42:00 GMT  
		Size: 8.4 KB (8358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d69d7dd59bb59dde508dbe82ea394fbbf613088f55858ffaff6298f6e91f2082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8162007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b49d45c13961b8773e2e5bfe4aae70fc3770bd0bbe0272f243bc7f5e76fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:75d8da399c93b2b984d9accb99f333d21162055db8115ba89f6917f944cfa353`  
		Last Modified: Mon, 07 Jul 2025 22:48:16 GMT  
		Size: 8.2 MB (8150035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e19c8ae070fa0a130cefd4738882cf0db6f79c15295390cf28a57688da1f28`  
		Last Modified: Mon, 07 Jul 2025 22:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250706.0.377547`

```console
$ docker pull archlinux@sha256:7ca06cad29fe509ea1b4a0fb40485ca410fe5fdbea39888c5f3169b4961b2b14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250706.0.377547` - linux; amd64

```console
$ docker pull archlinux@sha256:9c1cd902a49c2fa899622c286cba954f82b95b00abc1d9e094103eed3600594a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163274141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac8e88fb26b28530e3448585327a70fe5d414f5af5f91c60a455dfd1042338`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e4655ef3515a3583f60522ea0db589115ae05d3ea8243775d40be9fd671a514a`  
		Last Modified: Mon, 07 Jul 2025 22:48:31 GMT  
		Size: 163.3 MB (163265783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7df37c7b4083f7f8c7c1ed77b16aa0f7e02318ac65fa5a6ce1a136eed4439`  
		Last Modified: Mon, 07 Jul 2025 20:42:00 GMT  
		Size: 8.4 KB (8358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250706.0.377547` - unknown; unknown

```console
$ docker pull archlinux@sha256:d69d7dd59bb59dde508dbe82ea394fbbf613088f55858ffaff6298f6e91f2082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8162007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b49d45c13961b8773e2e5bfe4aae70fc3770bd0bbe0272f243bc7f5e76fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:75d8da399c93b2b984d9accb99f333d21162055db8115ba89f6917f944cfa353`  
		Last Modified: Mon, 07 Jul 2025 22:48:16 GMT  
		Size: 8.2 MB (8150035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e19c8ae070fa0a130cefd4738882cf0db6f79c15295390cf28a57688da1f28`  
		Last Modified: Mon, 07 Jul 2025 22:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:7beca11cc5203d0d7ee2e1202637f2600233b9e6195209f503d42ba356d414e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5c69359f124f1cf8a9893316275a365d3e385bedefb14b303b05dc32c756a62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (287989756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50566aeecbb8d701123cb31d46526e372d2cd8335c206a50a2344364b537349d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9f0d5de9ddb4d81aa2a08509561163ca7693879d92ac0b865ce0886de4c37f32`  
		Last Modified: Mon, 07 Jul 2025 22:53:36 GMT  
		Size: 288.0 MB (287980592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592358f41916bd8be2c671e8d2fa64d6177220b1c122ccd0a7ff526d0ba6f4b3`  
		Last Modified: Mon, 07 Jul 2025 20:42:39 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:592c70285fb2f9541e249d9b36fb83fdd6af648ddf902502ddf23bce643e823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12023256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cab1edfec4b64f88b3e28bf3619d1a440b7de9f7656c72e9d06b0894761aad`

```dockerfile
```

-	Layers:
	-	`sha256:486429721b9f31a7973dea12cfccc79d6002d6d1d82204e6192dc655ebe4bd9d`  
		Last Modified: Mon, 07 Jul 2025 22:48:20 GMT  
		Size: 12.0 MB (12011502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5bbdf1f466f6084825933d45522be922045282ab20746134f5a45922a972c0`  
		Last Modified: Mon, 07 Jul 2025 22:48:21 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250706.0.377547`

```console
$ docker pull archlinux@sha256:7beca11cc5203d0d7ee2e1202637f2600233b9e6195209f503d42ba356d414e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250706.0.377547` - linux; amd64

```console
$ docker pull archlinux@sha256:5c69359f124f1cf8a9893316275a365d3e385bedefb14b303b05dc32c756a62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (287989756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50566aeecbb8d701123cb31d46526e372d2cd8335c206a50a2344364b537349d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9f0d5de9ddb4d81aa2a08509561163ca7693879d92ac0b865ce0886de4c37f32`  
		Last Modified: Mon, 07 Jul 2025 22:53:36 GMT  
		Size: 288.0 MB (287980592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592358f41916bd8be2c671e8d2fa64d6177220b1c122ccd0a7ff526d0ba6f4b3`  
		Last Modified: Mon, 07 Jul 2025 20:42:39 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250706.0.377547` - unknown; unknown

```console
$ docker pull archlinux@sha256:592c70285fb2f9541e249d9b36fb83fdd6af648ddf902502ddf23bce643e823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12023256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cab1edfec4b64f88b3e28bf3619d1a440b7de9f7656c72e9d06b0894761aad`

```dockerfile
```

-	Layers:
	-	`sha256:486429721b9f31a7973dea12cfccc79d6002d6d1d82204e6192dc655ebe4bd9d`  
		Last Modified: Mon, 07 Jul 2025 22:48:20 GMT  
		Size: 12.0 MB (12011502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5bbdf1f466f6084825933d45522be922045282ab20746134f5a45922a972c0`  
		Last Modified: Mon, 07 Jul 2025 22:48:21 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:7ca06cad29fe509ea1b4a0fb40485ca410fe5fdbea39888c5f3169b4961b2b14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9c1cd902a49c2fa899622c286cba954f82b95b00abc1d9e094103eed3600594a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163274141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac8e88fb26b28530e3448585327a70fe5d414f5af5f91c60a455dfd1042338`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e4655ef3515a3583f60522ea0db589115ae05d3ea8243775d40be9fd671a514a`  
		Last Modified: Mon, 07 Jul 2025 22:48:31 GMT  
		Size: 163.3 MB (163265783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7df37c7b4083f7f8c7c1ed77b16aa0f7e02318ac65fa5a6ce1a136eed4439`  
		Last Modified: Mon, 07 Jul 2025 20:42:00 GMT  
		Size: 8.4 KB (8358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d69d7dd59bb59dde508dbe82ea394fbbf613088f55858ffaff6298f6e91f2082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8162007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b49d45c13961b8773e2e5bfe4aae70fc3770bd0bbe0272f243bc7f5e76fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:75d8da399c93b2b984d9accb99f333d21162055db8115ba89f6917f944cfa353`  
		Last Modified: Mon, 07 Jul 2025 22:48:16 GMT  
		Size: 8.2 MB (8150035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e19c8ae070fa0a130cefd4738882cf0db6f79c15295390cf28a57688da1f28`  
		Last Modified: Mon, 07 Jul 2025 22:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:8e2026123f027a115b7a0f77d2dc6a8b6e2432681d9362506e24a4cf66eeb10d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:910dd2c30735771a6939a5bec6c9e3983edbf52d71217515861024dfa96b035e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339156701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662187e8fa94c93225e4f441c71d120988ee206404f5ad169648b4b639d99ffe`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6b021388ae3bc2cffb6dc29835ef55bf7407e0b696e9b961f8d1116618fd8d70`  
		Last Modified: Tue, 08 Jul 2025 00:07:29 GMT  
		Size: 339.1 MB (339146422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78db3818f1db2189e0a57f97efea2333e9b61e5a8d3c3d6b9e54ce3f31e4742`  
		Last Modified: Mon, 07 Jul 2025 20:42:47 GMT  
		Size: 10.3 KB (10279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:91cbc873824ad65fe3474dc1f5a45f64519e569b521fc12cb4055a0acb8b8d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12292202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a365bd922e9a109f43e2ca18aa38a5493ce724c5115cd5e400a3a169fd0cd4`

```dockerfile
```

-	Layers:
	-	`sha256:cda3835e97859e858bc6cbfd7d9fc5feb27b63f699ce1c810fc4a0a754ce9d94`  
		Last Modified: Mon, 07 Jul 2025 22:48:25 GMT  
		Size: 12.3 MB (12280391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a221803e31b8bcf6e39316220cbb37a5ff5a078f60ada706e433fa0211620f4`  
		Last Modified: Mon, 07 Jul 2025 22:48:27 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250706.0.377547`

```console
$ docker pull archlinux@sha256:8e2026123f027a115b7a0f77d2dc6a8b6e2432681d9362506e24a4cf66eeb10d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250706.0.377547` - linux; amd64

```console
$ docker pull archlinux@sha256:910dd2c30735771a6939a5bec6c9e3983edbf52d71217515861024dfa96b035e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339156701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662187e8fa94c93225e4f441c71d120988ee206404f5ad169648b4b639d99ffe`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6b021388ae3bc2cffb6dc29835ef55bf7407e0b696e9b961f8d1116618fd8d70`  
		Last Modified: Tue, 08 Jul 2025 00:07:29 GMT  
		Size: 339.1 MB (339146422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78db3818f1db2189e0a57f97efea2333e9b61e5a8d3c3d6b9e54ce3f31e4742`  
		Last Modified: Mon, 07 Jul 2025 20:42:47 GMT  
		Size: 10.3 KB (10279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250706.0.377547` - unknown; unknown

```console
$ docker pull archlinux@sha256:91cbc873824ad65fe3474dc1f5a45f64519e569b521fc12cb4055a0acb8b8d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12292202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a365bd922e9a109f43e2ca18aa38a5493ce724c5115cd5e400a3a169fd0cd4`

```dockerfile
```

-	Layers:
	-	`sha256:cda3835e97859e858bc6cbfd7d9fc5feb27b63f699ce1c810fc4a0a754ce9d94`  
		Last Modified: Mon, 07 Jul 2025 22:48:25 GMT  
		Size: 12.3 MB (12280391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a221803e31b8bcf6e39316220cbb37a5ff5a078f60ada706e433fa0211620f4`  
		Last Modified: Mon, 07 Jul 2025 22:48:27 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
