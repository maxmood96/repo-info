<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20251214.0.467559`](#archlinuxbase-202512140467559)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20251214.0.467559`](#archlinuxbase-devel-202512140467559)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20251214.0.467559`](#archlinuxmultilib-devel-202512140467559)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:cbda7ef1fe6738d94dcae2bac2c6bc28978b2a41c24773f5cf73f58fa9986078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:42a51c3da6340ad79480f7db1fcc58fd77d4f38016f1155f4361954416ebcf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174525091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a51b69982e7d358e00530615c2f5b52948ff9242f2dc5cac06f4669e20c971`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:31:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:31:53 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:31:53 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:31:53 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f01404d5588892b3d97f4e80816575127ee71f0db9920a3765dc85e0df6538e3`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 174.5 MB (174516414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c119f11fe6f01b611131f168c8e326d034460637feb832b8bc9bb8f73ec79b81`  
		Last Modified: Mon, 15 Dec 2025 18:32:42 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:576d378ca9e9738a8642a05ce7c94c83ecb0d12403637478e72105ea1a2803a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8380747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c806ff195fe88dfd2d95b3c6bf2e4c4ff1014feea828fe72d6ae397c3511269c`

```dockerfile
```

-	Layers:
	-	`sha256:188106a5390cec650c09c7625e5fe3c6b614be676edb3fc733f0a91bcea34041`  
		Last Modified: Mon, 15 Dec 2025 20:48:16 GMT  
		Size: 8.4 MB (8368818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48ea3967ab3185e964cb5d8d68b3ae50c41bf41f0b4054b7456e3e0e4364ce8`  
		Last Modified: Mon, 15 Dec 2025 20:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251214.0.467559`

```console
$ docker pull archlinux@sha256:cbda7ef1fe6738d94dcae2bac2c6bc28978b2a41c24773f5cf73f58fa9986078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20251214.0.467559` - linux; amd64

```console
$ docker pull archlinux@sha256:42a51c3da6340ad79480f7db1fcc58fd77d4f38016f1155f4361954416ebcf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174525091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a51b69982e7d358e00530615c2f5b52948ff9242f2dc5cac06f4669e20c971`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:31:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:31:53 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:31:53 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:31:53 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f01404d5588892b3d97f4e80816575127ee71f0db9920a3765dc85e0df6538e3`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 174.5 MB (174516414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c119f11fe6f01b611131f168c8e326d034460637feb832b8bc9bb8f73ec79b81`  
		Last Modified: Mon, 15 Dec 2025 18:32:42 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20251214.0.467559` - unknown; unknown

```console
$ docker pull archlinux@sha256:576d378ca9e9738a8642a05ce7c94c83ecb0d12403637478e72105ea1a2803a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8380747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c806ff195fe88dfd2d95b3c6bf2e4c4ff1014feea828fe72d6ae397c3511269c`

```dockerfile
```

-	Layers:
	-	`sha256:188106a5390cec650c09c7625e5fe3c6b614be676edb3fc733f0a91bcea34041`  
		Last Modified: Mon, 15 Dec 2025 20:48:16 GMT  
		Size: 8.4 MB (8368818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48ea3967ab3185e964cb5d8d68b3ae50c41bf41f0b4054b7456e3e0e4364ce8`  
		Last Modified: Mon, 15 Dec 2025 20:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:1635f3838c665558a2aaac32929470ef844f65be4acd5c47167c6d98d74baba2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3933d17afd7338682a5c67314e8cf4ba91a48d184264899b25e60ed4d8e68fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f17cb5ace583a497da558773ee52a532df623ede60a1a4308f51751649c7df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:32:17 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:32:24 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:32:24 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:32:24 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:28f03c6e8bb3a7030933065fad15d28b50b0bfc498ea6d4cedd92904feb81e22`  
		Last Modified: Mon, 15 Dec 2025 18:33:53 GMT  
		Size: 292.1 MB (292061547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e72afe4396e320604700a6d169207768e63d8b10b9db29238ad97c87ba906d4`  
		Last Modified: Mon, 15 Dec 2025 18:33:31 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:fc6186dd7214c50da7f91d520c46a383c3afa34531378ed11196ad1fe36478b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12142872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bda182f627f017a73b44b44a745ee4dc6df88ef22da981674c66fe9d804eed`

```dockerfile
```

-	Layers:
	-	`sha256:8d4a87d4642d8c4bafe737c0bed5c913d0f6ffd5e158140c2ed521500c86590d`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 12.1 MB (12131161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe7dc55e0051978bd4d4d28c0ce9d9eb840053e74da2febbba86a1c62e64ce5`  
		Last Modified: Mon, 15 Dec 2025 20:48:24 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251214.0.467559`

```console
$ docker pull archlinux@sha256:1635f3838c665558a2aaac32929470ef844f65be4acd5c47167c6d98d74baba2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251214.0.467559` - linux; amd64

```console
$ docker pull archlinux@sha256:3933d17afd7338682a5c67314e8cf4ba91a48d184264899b25e60ed4d8e68fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f17cb5ace583a497da558773ee52a532df623ede60a1a4308f51751649c7df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:32:17 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:32:17 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:32:24 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:32:24 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:32:24 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:28f03c6e8bb3a7030933065fad15d28b50b0bfc498ea6d4cedd92904feb81e22`  
		Last Modified: Mon, 15 Dec 2025 18:33:53 GMT  
		Size: 292.1 MB (292061547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e72afe4396e320604700a6d169207768e63d8b10b9db29238ad97c87ba906d4`  
		Last Modified: Mon, 15 Dec 2025 18:33:31 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251214.0.467559` - unknown; unknown

```console
$ docker pull archlinux@sha256:fc6186dd7214c50da7f91d520c46a383c3afa34531378ed11196ad1fe36478b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12142872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bda182f627f017a73b44b44a745ee4dc6df88ef22da981674c66fe9d804eed`

```dockerfile
```

-	Layers:
	-	`sha256:8d4a87d4642d8c4bafe737c0bed5c913d0f6ffd5e158140c2ed521500c86590d`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 12.1 MB (12131161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe7dc55e0051978bd4d4d28c0ce9d9eb840053e74da2febbba86a1c62e64ce5`  
		Last Modified: Mon, 15 Dec 2025 20:48:24 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:cbda7ef1fe6738d94dcae2bac2c6bc28978b2a41c24773f5cf73f58fa9986078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:42a51c3da6340ad79480f7db1fcc58fd77d4f38016f1155f4361954416ebcf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174525091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a51b69982e7d358e00530615c2f5b52948ff9242f2dc5cac06f4669e20c971`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:31:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:31:53 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:31:53 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:31:53 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f01404d5588892b3d97f4e80816575127ee71f0db9920a3765dc85e0df6538e3`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 174.5 MB (174516414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c119f11fe6f01b611131f168c8e326d034460637feb832b8bc9bb8f73ec79b81`  
		Last Modified: Mon, 15 Dec 2025 18:32:42 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:576d378ca9e9738a8642a05ce7c94c83ecb0d12403637478e72105ea1a2803a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8380747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c806ff195fe88dfd2d95b3c6bf2e4c4ff1014feea828fe72d6ae397c3511269c`

```dockerfile
```

-	Layers:
	-	`sha256:188106a5390cec650c09c7625e5fe3c6b614be676edb3fc733f0a91bcea34041`  
		Last Modified: Mon, 15 Dec 2025 20:48:16 GMT  
		Size: 8.4 MB (8368818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48ea3967ab3185e964cb5d8d68b3ae50c41bf41f0b4054b7456e3e0e4364ce8`  
		Last Modified: Mon, 15 Dec 2025 20:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:e6f380814330655127d3992645edea1f3eedbb64ebc104c1720cab5ba5b8edc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8469ab5c69f1418d7d383f8efed700dc534a0c805318fa6c2a2d3a75f801be5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343393692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e88f1c7781849036177cd9cab713eff2f6bc6532c8b239357d60f1dd9b930e9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:33:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:33:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:33:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:33:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7b1e20b4fe65799151a60bf5d121f5f6f83fcd2aca9d80b1b2515a189308c3fd`  
		Last Modified: Mon, 15 Dec 2025 18:34:37 GMT  
		Size: 343.4 MB (343383370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac785afd68e3d429e4a59200c9e62541df8f9ebe66a65d85c9944e885b89ceaf`  
		Last Modified: Mon, 15 Dec 2025 18:34:28 GMT  
		Size: 10.3 KB (10322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:734e6d85dff9efb2f64c23577d82df79d53f939e36b4c76f12109a73dda8a89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12411721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecec4fa283964a4341ef8428286b33c6a0ffc909779810155c0d6b27717c18a`

```dockerfile
```

-	Layers:
	-	`sha256:596d9cf7986b992d90f6ff15fafbccc6568ed3ab316908216ff6cdeb4bebf85c`  
		Last Modified: Mon, 15 Dec 2025 20:48:30 GMT  
		Size: 12.4 MB (12399954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ced505fb617f128419ebe504694162a1a214ad01a774ed1720bdb86c3d61dfe`  
		Last Modified: Mon, 15 Dec 2025 20:48:31 GMT  
		Size: 11.8 KB (11767 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251214.0.467559`

```console
$ docker pull archlinux@sha256:e6f380814330655127d3992645edea1f3eedbb64ebc104c1720cab5ba5b8edc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251214.0.467559` - linux; amd64

```console
$ docker pull archlinux@sha256:8469ab5c69f1418d7d383f8efed700dc534a0c805318fa6c2a2d3a75f801be5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343393692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e88f1c7781849036177cd9cab713eff2f6bc6532c8b239357d60f1dd9b930e9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:33:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:33:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:33:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:33:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7b1e20b4fe65799151a60bf5d121f5f6f83fcd2aca9d80b1b2515a189308c3fd`  
		Last Modified: Mon, 15 Dec 2025 18:34:37 GMT  
		Size: 343.4 MB (343383370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac785afd68e3d429e4a59200c9e62541df8f9ebe66a65d85c9944e885b89ceaf`  
		Last Modified: Mon, 15 Dec 2025 18:34:28 GMT  
		Size: 10.3 KB (10322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251214.0.467559` - unknown; unknown

```console
$ docker pull archlinux@sha256:734e6d85dff9efb2f64c23577d82df79d53f939e36b4c76f12109a73dda8a89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12411721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecec4fa283964a4341ef8428286b33c6a0ffc909779810155c0d6b27717c18a`

```dockerfile
```

-	Layers:
	-	`sha256:596d9cf7986b992d90f6ff15fafbccc6568ed3ab316908216ff6cdeb4bebf85c`  
		Last Modified: Mon, 15 Dec 2025 20:48:30 GMT  
		Size: 12.4 MB (12399954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ced505fb617f128419ebe504694162a1a214ad01a774ed1720bdb86c3d61dfe`  
		Last Modified: Mon, 15 Dec 2025 20:48:31 GMT  
		Size: 11.8 KB (11767 bytes)  
		MIME: application/vnd.in-toto+json
