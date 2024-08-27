<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240825.0.257728`](#archlinuxbase-202408250257728)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240825.0.257728`](#archlinuxbase-devel-202408250257728)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240825.0.257728`](#archlinuxmultilib-devel-202408250257728)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:7dba90fa0171e5f23fd41500f15263b61bf4f95464f527d7152e15cb35e7a7d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:2040d6337505c204e3991f509e62f728d8b4d465e9f8379815dce117c464143b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151183315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959149ca6d710bb267e4025fdc80deafc201371adab763a606162c80367e9dc7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a7eeb2be9236376dfb256be5af295b286214fd6f9583c91a99e5de0a412b7dd`  
		Last Modified: Mon, 26 Aug 2024 21:59:19 GMT  
		Size: 151.2 MB (151175032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a9bc48d5fff4402023f6b618fdb83fd6b9a9b04f7c497cd062bb71be893b7d`  
		Last Modified: Mon, 26 Aug 2024 21:59:14 GMT  
		Size: 8.3 KB (8283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:10c1a6c09dbf2bd280b93d450f89ef49a8549ba4afcf1cbabc415c8f7a693366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1894bddefaab455d063d2508dd1891b6a343b81910c306fd2c9d0a5e8e74771`

```dockerfile
```

-	Layers:
	-	`sha256:12310cb0423ae8a5202e44d31c72d2e24683851a2e5bdee85393f4c62e20341a`  
		Last Modified: Mon, 26 Aug 2024 21:59:15 GMT  
		Size: 8.1 MB (8103979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acaeace8729b8b4f553c93549de5f6ddd4fc67c093f72be7f207096a840d51e`  
		Last Modified: Mon, 26 Aug 2024 21:59:14 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240825.0.257728`

```console
$ docker pull archlinux@sha256:7dba90fa0171e5f23fd41500f15263b61bf4f95464f527d7152e15cb35e7a7d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20240825.0.257728` - linux; amd64

```console
$ docker pull archlinux@sha256:2040d6337505c204e3991f509e62f728d8b4d465e9f8379815dce117c464143b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151183315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959149ca6d710bb267e4025fdc80deafc201371adab763a606162c80367e9dc7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a7eeb2be9236376dfb256be5af295b286214fd6f9583c91a99e5de0a412b7dd`  
		Last Modified: Mon, 26 Aug 2024 21:59:19 GMT  
		Size: 151.2 MB (151175032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a9bc48d5fff4402023f6b618fdb83fd6b9a9b04f7c497cd062bb71be893b7d`  
		Last Modified: Mon, 26 Aug 2024 21:59:14 GMT  
		Size: 8.3 KB (8283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20240825.0.257728` - unknown; unknown

```console
$ docker pull archlinux@sha256:10c1a6c09dbf2bd280b93d450f89ef49a8549ba4afcf1cbabc415c8f7a693366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1894bddefaab455d063d2508dd1891b6a343b81910c306fd2c9d0a5e8e74771`

```dockerfile
```

-	Layers:
	-	`sha256:12310cb0423ae8a5202e44d31c72d2e24683851a2e5bdee85393f4c62e20341a`  
		Last Modified: Mon, 26 Aug 2024 21:59:15 GMT  
		Size: 8.1 MB (8103979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acaeace8729b8b4f553c93549de5f6ddd4fc67c093f72be7f207096a840d51e`  
		Last Modified: Mon, 26 Aug 2024 21:59:14 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0a0024b86e4ec09652a3d98b1523509cfbbe47edea464ec775f41c8a506611bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4cf6853663815a5fc6b71ec234c4c3c56570bf325e54ffa298c4b701173aa3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271737229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff2dc87c647fce56a19da956611bbe7a811017385d380250806b60b374b047d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:298dc0d2952244fad2540d1cd7765c9b3beb1fae3ae90fe74a9d3339125caf9b`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 271.7 MB (271728156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f652bae07bffcc8cfb894cf4f7bd10f8673e0ea5c49e087c9aad788dee476`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 9.1 KB (9073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:5dd1f62fab40309d3c7719203468ea51cad8e9e035d003dcb22561e21fc4e419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2562e9d770065dce7da13b06599ae58a1b08eca07cd3e524130caca2731142`

```dockerfile
```

-	Layers:
	-	`sha256:d1ffce5987530f281d0a6301f0592673236753a4e6af168a8e76d1bdc308fe72`  
		Last Modified: Mon, 26 Aug 2024 21:59:45 GMT  
		Size: 11.8 MB (11818188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef528f73d1ed1046bbdaf5dc47836287c8a5f5e5ba04e59006c303cd0baf0537`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 11.5 KB (11502 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240825.0.257728`

```console
$ docker pull archlinux@sha256:0a0024b86e4ec09652a3d98b1523509cfbbe47edea464ec775f41c8a506611bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240825.0.257728` - linux; amd64

```console
$ docker pull archlinux@sha256:4cf6853663815a5fc6b71ec234c4c3c56570bf325e54ffa298c4b701173aa3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271737229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff2dc87c647fce56a19da956611bbe7a811017385d380250806b60b374b047d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:298dc0d2952244fad2540d1cd7765c9b3beb1fae3ae90fe74a9d3339125caf9b`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 271.7 MB (271728156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f652bae07bffcc8cfb894cf4f7bd10f8673e0ea5c49e087c9aad788dee476`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 9.1 KB (9073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240825.0.257728` - unknown; unknown

```console
$ docker pull archlinux@sha256:5dd1f62fab40309d3c7719203468ea51cad8e9e035d003dcb22561e21fc4e419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2562e9d770065dce7da13b06599ae58a1b08eca07cd3e524130caca2731142`

```dockerfile
```

-	Layers:
	-	`sha256:d1ffce5987530f281d0a6301f0592673236753a4e6af168a8e76d1bdc308fe72`  
		Last Modified: Mon, 26 Aug 2024 21:59:45 GMT  
		Size: 11.8 MB (11818188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef528f73d1ed1046bbdaf5dc47836287c8a5f5e5ba04e59006c303cd0baf0537`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 11.5 KB (11502 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:7dba90fa0171e5f23fd41500f15263b61bf4f95464f527d7152e15cb35e7a7d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2040d6337505c204e3991f509e62f728d8b4d465e9f8379815dce117c464143b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151183315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959149ca6d710bb267e4025fdc80deafc201371adab763a606162c80367e9dc7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a7eeb2be9236376dfb256be5af295b286214fd6f9583c91a99e5de0a412b7dd`  
		Last Modified: Mon, 26 Aug 2024 21:59:19 GMT  
		Size: 151.2 MB (151175032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a9bc48d5fff4402023f6b618fdb83fd6b9a9b04f7c497cd062bb71be893b7d`  
		Last Modified: Mon, 26 Aug 2024 21:59:14 GMT  
		Size: 8.3 KB (8283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:10c1a6c09dbf2bd280b93d450f89ef49a8549ba4afcf1cbabc415c8f7a693366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1894bddefaab455d063d2508dd1891b6a343b81910c306fd2c9d0a5e8e74771`

```dockerfile
```

-	Layers:
	-	`sha256:12310cb0423ae8a5202e44d31c72d2e24683851a2e5bdee85393f4c62e20341a`  
		Last Modified: Mon, 26 Aug 2024 21:59:15 GMT  
		Size: 8.1 MB (8103979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acaeace8729b8b4f553c93549de5f6ddd4fc67c093f72be7f207096a840d51e`  
		Last Modified: Mon, 26 Aug 2024 21:59:14 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:787247c74479f2dadbd1a1a336e0c26d8312d54f884afc67b29bba5bde56e995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:16d590427240779ff96610a996f2acc10041ee17d59c90dab981257e47bd0aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321627592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cce18feb462cc0ce674952344569566b6d3b781192af2dede313cbb971424f9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b39c3f3d5831908f56eae8d8bceedb49c7424402515d9cf9b1feb3ba6c022781`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 321.6 MB (321617407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34176b4a87a58fee083b819f8974173ec092d49362333ea31c72a416a8627019`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 10.2 KB (10185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:b00b1a08a255a55cefb94284cfddd986f1d06d995c83a826c7aa3aeea42ac9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b3d81cb60807ca62152dc5bc418444bc5920f97fd9b43f54787f51762401a5`

```dockerfile
```

-	Layers:
	-	`sha256:84e929d0df5ed6d0a81c6ddd964836dcf541ba6592fe33e93831a489960b988d`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 12.1 MB (12085490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056aa45e388121c0566282711b40861fe85dfd388a0eb377497b49857547d658`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240825.0.257728`

```console
$ docker pull archlinux@sha256:787247c74479f2dadbd1a1a336e0c26d8312d54f884afc67b29bba5bde56e995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240825.0.257728` - linux; amd64

```console
$ docker pull archlinux@sha256:16d590427240779ff96610a996f2acc10041ee17d59c90dab981257e47bd0aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321627592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cce18feb462cc0ce674952344569566b6d3b781192af2dede313cbb971424f9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b39c3f3d5831908f56eae8d8bceedb49c7424402515d9cf9b1feb3ba6c022781`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 321.6 MB (321617407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34176b4a87a58fee083b819f8974173ec092d49362333ea31c72a416a8627019`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 10.2 KB (10185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240825.0.257728` - unknown; unknown

```console
$ docker pull archlinux@sha256:b00b1a08a255a55cefb94284cfddd986f1d06d995c83a826c7aa3aeea42ac9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b3d81cb60807ca62152dc5bc418444bc5920f97fd9b43f54787f51762401a5`

```dockerfile
```

-	Layers:
	-	`sha256:84e929d0df5ed6d0a81c6ddd964836dcf541ba6592fe33e93831a489960b988d`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 12.1 MB (12085490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056aa45e388121c0566282711b40861fe85dfd388a0eb377497b49857547d658`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
