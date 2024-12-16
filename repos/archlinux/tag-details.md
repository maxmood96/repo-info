<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241215.0.289170`](#archlinuxbase-202412150289170)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241215.0.289170`](#archlinuxbase-devel-202412150289170)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241215.0.289170`](#archlinuxmultilib-devel-202412150289170)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:5906892165fc79b4e282e36f24802528bcee2bd2896982ad771045341e15db5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0ad2f00a305657ced5001f8d41d3dfd6429a8069e4bb3eab890dc232537719ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152291760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8964901e692515f9bdd5bb6d16e6cb3af6739a6fc6afb3ef299f42411b15a85b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.version=20241208.0.286830
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.created=2024-12-08T00:07:49+00:00
# Sun, 08 Dec 2024 00:07:49 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241208.0.286830' /etc/os-release # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
ENV LANG=C.UTF-8
# Sun, 08 Dec 2024 00:07:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a657cefe89310565e146e5ba7877550e1460875ce9c57e91c29918efa9e922a0`  
		Last Modified: Mon, 09 Dec 2024 19:28:35 GMT  
		Size: 152.3 MB (152283443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf988a8d22c1d5021726e9d622a45c020c406f160ae3a8eb4096a6772f75f7d`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:4ea970ea8d720070e3faa9bbd7c8bbbca96a82cd3a114d697cfa97ac56c90257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8095271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab491e7d7847963c80975ff0fc5de6c820de1df7806af8e2963d9625b14b736`

```dockerfile
```

-	Layers:
	-	`sha256:e28dc204826342bda6e9648087fc071d774364d5a3db020d143b779bc4327a68`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 8.1 MB (8083299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac5064e13be4ec53093c68dba80349dc7347e674a4cfd7b6d9dd948355ceaa6`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241215.0.289170`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:ad7265dcfc77e1de728808f70b38af05f2e15af9d49e2bda7eb78c33c4af9f8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f2d673da953a7eafb0d6d0aaf0696ba6504b316cb6c266d2d1e6e1ec76a11ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273417914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc662799b750cee2550eb81a5cb5b892640c0e5ded2b4711a8519463b68fdbf3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.version=20241208.0.286830
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.created=2024-12-08T00:07:49+00:00
# Sun, 08 Dec 2024 00:07:49 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241208.0.286830' /etc/os-release # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
ENV LANG=C.UTF-8
# Sun, 08 Dec 2024 00:07:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4dddf33f2d22fe711bc3b375cc5bf972dcb73a808ac73e9580261bd89629b88e`  
		Last Modified: Mon, 09 Dec 2024 19:29:05 GMT  
		Size: 273.4 MB (273408836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6e8053ae34cf074b762d4d6648fca119c3913903624dd72675af890497a4a5`  
		Last Modified: Mon, 09 Dec 2024 19:29:01 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:56658971362ac1af8bd4787b6df9adec16854da79d419b9a1a9eb99fe159da10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9ed79f6e4e53dd39251af10cb392667c41c3760638c3c72c968fbc340b60e4`

```dockerfile
```

-	Layers:
	-	`sha256:a9892998169112e5dbc0db679e82e8c8ab5f304476aea015725973a0bff023f4`  
		Last Modified: Mon, 09 Dec 2024 19:29:01 GMT  
		Size: 11.9 MB (11896942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79615ce59fc128734ad8beb6b434c4f76d10ffb033d7d7d2f464ddd83f0b43ee`  
		Last Modified: Mon, 09 Dec 2024 19:29:01 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241215.0.289170`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:5906892165fc79b4e282e36f24802528bcee2bd2896982ad771045341e15db5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0ad2f00a305657ced5001f8d41d3dfd6429a8069e4bb3eab890dc232537719ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152291760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8964901e692515f9bdd5bb6d16e6cb3af6739a6fc6afb3ef299f42411b15a85b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.version=20241208.0.286830
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.created=2024-12-08T00:07:49+00:00
# Sun, 08 Dec 2024 00:07:49 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241208.0.286830' /etc/os-release # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
ENV LANG=C.UTF-8
# Sun, 08 Dec 2024 00:07:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a657cefe89310565e146e5ba7877550e1460875ce9c57e91c29918efa9e922a0`  
		Last Modified: Mon, 09 Dec 2024 19:28:35 GMT  
		Size: 152.3 MB (152283443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf988a8d22c1d5021726e9d622a45c020c406f160ae3a8eb4096a6772f75f7d`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:4ea970ea8d720070e3faa9bbd7c8bbbca96a82cd3a114d697cfa97ac56c90257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8095271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab491e7d7847963c80975ff0fc5de6c820de1df7806af8e2963d9625b14b736`

```dockerfile
```

-	Layers:
	-	`sha256:e28dc204826342bda6e9648087fc071d774364d5a3db020d143b779bc4327a68`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 8.1 MB (8083299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac5064e13be4ec53093c68dba80349dc7347e674a4cfd7b6d9dd948355ceaa6`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:331b6b59d467abd4147d96cce5e4e898f70831247535bb132c92bb42b9fc0e7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:98ae1574320b75c976dc1b06c8842b7f423a419a0412e52db57182f5e1204c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323274751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f71697d69e335877143ef3db8c9be57d5e65b1bb6cc3323d4d3c228048de09`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.version=20241208.0.286830
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.created=2024-12-08T00:07:49+00:00
# Sun, 08 Dec 2024 00:07:49 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241208.0.286830' /etc/os-release # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
ENV LANG=C.UTF-8
# Sun, 08 Dec 2024 00:07:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:85bf5fc2a5d09aa85a801947ae693f0790594124d9b5fec35315198a760bd3c9`  
		Last Modified: Mon, 09 Dec 2024 19:29:25 GMT  
		Size: 323.3 MB (323264555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6003d38f7667dc01b94e86f186c6b6991a0073ff6540a0a1d2f41b6bdd81b125`  
		Last Modified: Mon, 09 Dec 2024 19:29:20 GMT  
		Size: 10.2 KB (10196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:056279a3c32abee047977ed1d3fa4a7eb83f2cec748da7aaef170137039928a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12177618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8778e4469093ce2b77e8127d89850e12145115b7bf643a2bec6f31615398ae11`

```dockerfile
```

-	Layers:
	-	`sha256:2ef5e53052b4ca164a85cdcaccd97d2723f8c1ea6d31c8a7b1c9ae8f33b6d7f3`  
		Last Modified: Mon, 09 Dec 2024 19:29:20 GMT  
		Size: 12.2 MB (12165807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964d4d9ea5fb6ac9632b11d9980a82ce9d2550daed26b61509ca61bfc29fe570`  
		Last Modified: Mon, 09 Dec 2024 19:29:20 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241215.0.289170`

**does not exist** (yet?)
