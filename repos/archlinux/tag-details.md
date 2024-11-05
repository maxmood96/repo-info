<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241103.0.276161`](#archlinuxbase-202411030276161)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241103.0.276161`](#archlinuxbase-devel-202411030276161)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241103.0.276161`](#archlinuxmultilib-devel-202411030276161)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:876f1f601e5fe6ceda682ac9b0a8df06be695fe9e2c85d04f48a877f17e46b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:89639d3a2d102158ab5a6668dc340a6e5cf1acf12f78b55b508b8c38da461869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151290858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad78b172bfc727fc18ce09cce74fd6d4a8ad10c59b9b9413cf5c3edb778dbb7c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7304439b608ad119a822a6f2749be0e4b54b6c5c50120b1a68128aec0fe54ffc`  
		Last Modified: Mon, 04 Nov 2024 22:04:33 GMT  
		Size: 151.3 MB (151282558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcbeaf6513208b6048f8bbeeb0de6d113a1929a56d42de734c75663a9c8bdd1`  
		Last Modified: Mon, 04 Nov 2024 22:04:29 GMT  
		Size: 8.3 KB (8300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d9b5f14825ea774e8ef2679fb1e019a853037a93fb14677b2648d4f8b3921014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8970fad62e2319137e450f4343c170ab08155549250df72f2b338afa082f100`

```dockerfile
```

-	Layers:
	-	`sha256:1e57a5d6f7993e35f506921a12b9c8fedf8f523b519d8e9f726877b604f5f68b`  
		Last Modified: Mon, 04 Nov 2024 22:04:30 GMT  
		Size: 8.1 MB (8144185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76660bc2012d08e0e3a04b9a9b6c5e3b933dcbfa01252b0451f4c0e933e59afd`  
		Last Modified: Mon, 04 Nov 2024 22:04:29 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241103.0.276161`

```console
$ docker pull archlinux@sha256:876f1f601e5fe6ceda682ac9b0a8df06be695fe9e2c85d04f48a877f17e46b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20241103.0.276161` - linux; amd64

```console
$ docker pull archlinux@sha256:89639d3a2d102158ab5a6668dc340a6e5cf1acf12f78b55b508b8c38da461869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151290858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad78b172bfc727fc18ce09cce74fd6d4a8ad10c59b9b9413cf5c3edb778dbb7c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7304439b608ad119a822a6f2749be0e4b54b6c5c50120b1a68128aec0fe54ffc`  
		Last Modified: Mon, 04 Nov 2024 22:04:33 GMT  
		Size: 151.3 MB (151282558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcbeaf6513208b6048f8bbeeb0de6d113a1929a56d42de734c75663a9c8bdd1`  
		Last Modified: Mon, 04 Nov 2024 22:04:29 GMT  
		Size: 8.3 KB (8300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20241103.0.276161` - unknown; unknown

```console
$ docker pull archlinux@sha256:d9b5f14825ea774e8ef2679fb1e019a853037a93fb14677b2648d4f8b3921014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8970fad62e2319137e450f4343c170ab08155549250df72f2b338afa082f100`

```dockerfile
```

-	Layers:
	-	`sha256:1e57a5d6f7993e35f506921a12b9c8fedf8f523b519d8e9f726877b604f5f68b`  
		Last Modified: Mon, 04 Nov 2024 22:04:30 GMT  
		Size: 8.1 MB (8144185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76660bc2012d08e0e3a04b9a9b6c5e3b933dcbfa01252b0451f4c0e933e59afd`  
		Last Modified: Mon, 04 Nov 2024 22:04:29 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:2e394a68150cdde8d1c4f7f9d9a6a9d8e21fd56c041d8607003c53ffabf0aaa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:afb417afa1aa9433e5cbb534602c84724d936b54187eef1049dde903e762ceff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272414900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dceeedcc610103f29bcba2d6623c514263cb1f7d7af4ef7b9a76691321147e4c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4198ddba3601b79804e83b86e3bd89492c3560e4d2b70023f815a6c1da87d4fa`  
		Last Modified: Mon, 04 Nov 2024 22:04:48 GMT  
		Size: 272.4 MB (272405834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808f95be0a6a37bbfec58f9ba340d523244d539ed88dd902c5cfe843051b37a`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 9.1 KB (9066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:446a216eb8179bf22bd785e0e686c195dd071cd65957d97f2e5b359efa4671f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11969317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89434f94497f1ab173de723829496cb5b07a7f6811dda65f623c47f6acb8e4b2`

```dockerfile
```

-	Layers:
	-	`sha256:0da84a7317d277c17044fed3a2482b9ddd1acc30edbfbd8dc22fe81649074351`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 12.0 MB (11957780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68367567a5c40510009c8cc0193620d653143687b4ec518a3d71a5be5eca62e`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241103.0.276161`

```console
$ docker pull archlinux@sha256:2e394a68150cdde8d1c4f7f9d9a6a9d8e21fd56c041d8607003c53ffabf0aaa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241103.0.276161` - linux; amd64

```console
$ docker pull archlinux@sha256:afb417afa1aa9433e5cbb534602c84724d936b54187eef1049dde903e762ceff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272414900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dceeedcc610103f29bcba2d6623c514263cb1f7d7af4ef7b9a76691321147e4c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4198ddba3601b79804e83b86e3bd89492c3560e4d2b70023f815a6c1da87d4fa`  
		Last Modified: Mon, 04 Nov 2024 22:04:48 GMT  
		Size: 272.4 MB (272405834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808f95be0a6a37bbfec58f9ba340d523244d539ed88dd902c5cfe843051b37a`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 9.1 KB (9066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241103.0.276161` - unknown; unknown

```console
$ docker pull archlinux@sha256:446a216eb8179bf22bd785e0e686c195dd071cd65957d97f2e5b359efa4671f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11969317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89434f94497f1ab173de723829496cb5b07a7f6811dda65f623c47f6acb8e4b2`

```dockerfile
```

-	Layers:
	-	`sha256:0da84a7317d277c17044fed3a2482b9ddd1acc30edbfbd8dc22fe81649074351`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 12.0 MB (11957780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68367567a5c40510009c8cc0193620d653143687b4ec518a3d71a5be5eca62e`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:876f1f601e5fe6ceda682ac9b0a8df06be695fe9e2c85d04f48a877f17e46b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:89639d3a2d102158ab5a6668dc340a6e5cf1acf12f78b55b508b8c38da461869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151290858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad78b172bfc727fc18ce09cce74fd6d4a8ad10c59b9b9413cf5c3edb778dbb7c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7304439b608ad119a822a6f2749be0e4b54b6c5c50120b1a68128aec0fe54ffc`  
		Last Modified: Mon, 04 Nov 2024 22:04:33 GMT  
		Size: 151.3 MB (151282558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcbeaf6513208b6048f8bbeeb0de6d113a1929a56d42de734c75663a9c8bdd1`  
		Last Modified: Mon, 04 Nov 2024 22:04:29 GMT  
		Size: 8.3 KB (8300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d9b5f14825ea774e8ef2679fb1e019a853037a93fb14677b2648d4f8b3921014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8970fad62e2319137e450f4343c170ab08155549250df72f2b338afa082f100`

```dockerfile
```

-	Layers:
	-	`sha256:1e57a5d6f7993e35f506921a12b9c8fedf8f523b519d8e9f726877b604f5f68b`  
		Last Modified: Mon, 04 Nov 2024 22:04:30 GMT  
		Size: 8.1 MB (8144185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76660bc2012d08e0e3a04b9a9b6c5e3b933dcbfa01252b0451f4c0e933e59afd`  
		Last Modified: Mon, 04 Nov 2024 22:04:29 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:b9eb0459c6e380b3c92e155654e06d7c3107a9691ac7d091275861d1994fae51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:a0f12e0add3c48afc4be7a4ccb87a19252bdb721fe2efc8f44ba606671ae8783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322266339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559d9693277569132d87b31d9a5b2314bf13f2e14fbbd530dac227b9a0838af7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ee64a7811103c061f3a30fb81cfeffb7ffd494c90867c065f6ad59738ad625b1`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 322.3 MB (322256125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72519b37c903eecf6bd5206c532180689bd474c9224cb998d54b4be00d4d7bf1`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 10.2 KB (10214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:96b7999c362e61e95a67ad9700de818d9e2b994c64566a39791153596b945921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12238170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7558523368ec36f23e46ccf711607b066c90a75b86ff5746e08e65c1c564c24`

```dockerfile
```

-	Layers:
	-	`sha256:a9320fcab8f22f17c5c4bb31bac425c7e82962e65efb135e6b8aa1890f3a2ff8`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 12.2 MB (12226576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc6b53b3d837c4b83fa6994ebc59bcb678bf26eebfc7e080e4d0c530d9ffb79`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241103.0.276161`

```console
$ docker pull archlinux@sha256:b9eb0459c6e380b3c92e155654e06d7c3107a9691ac7d091275861d1994fae51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241103.0.276161` - linux; amd64

```console
$ docker pull archlinux@sha256:a0f12e0add3c48afc4be7a4ccb87a19252bdb721fe2efc8f44ba606671ae8783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322266339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559d9693277569132d87b31d9a5b2314bf13f2e14fbbd530dac227b9a0838af7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ee64a7811103c061f3a30fb81cfeffb7ffd494c90867c065f6ad59738ad625b1`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 322.3 MB (322256125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72519b37c903eecf6bd5206c532180689bd474c9224cb998d54b4be00d4d7bf1`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 10.2 KB (10214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241103.0.276161` - unknown; unknown

```console
$ docker pull archlinux@sha256:96b7999c362e61e95a67ad9700de818d9e2b994c64566a39791153596b945921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12238170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7558523368ec36f23e46ccf711607b066c90a75b86ff5746e08e65c1c564c24`

```dockerfile
```

-	Layers:
	-	`sha256:a9320fcab8f22f17c5c4bb31bac425c7e82962e65efb135e6b8aa1890f3a2ff8`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 12.2 MB (12226576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc6b53b3d837c4b83fa6994ebc59bcb678bf26eebfc7e080e4d0c530d9ffb79`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json
