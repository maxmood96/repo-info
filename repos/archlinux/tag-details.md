<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240721.0.248532`](#archlinuxbase-202407210248532)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240721.0.248532`](#archlinuxbase-devel-202407210248532)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240721.0.248532`](#archlinuxmultilib-devel-202407210248532)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:76fbb2a91a9c06b05372eb2c2e0a0edf19a864258284e2dad2002c96f776c031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:26355e4be5736c53efac48531b80d0ea1b32513e7e5d972098dd21a17cd72e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151088780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e895e05153b430a2a12984c31a25e52e9d23ab3bc71f1a314ccca1dd2171ae7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d60d5665bb190f639c1d4f286977018d4342bc47593af30e0b92968fe432d0bc`  
		Last Modified: Mon, 22 Jul 2024 19:59:06 GMT  
		Size: 151.1 MB (151080489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56de0cb20f43c946371788cf57a2e4218c3aef7c9f3b5e136296f03f54645dfb`  
		Last Modified: Mon, 22 Jul 2024 19:59:03 GMT  
		Size: 8.3 KB (8291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:73075f0609136245902753e42fecec5b3bfcbd6bc13fbc7d518eb17bd66b4955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f95a0f7c288ccfb9d74945c79034e1da3d3df3b73508815159f4b796787a5f`

```dockerfile
```

-	Layers:
	-	`sha256:29241b1b22ea97bde5a201e66a13d3fdf2048792ab418e5f03ac7f197a0a9a88`  
		Last Modified: Mon, 22 Jul 2024 19:59:04 GMT  
		Size: 8.1 MB (8098505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5030466b8633e0e22c1645a53d8de4cb31d8fb8a7026642e5e524adbbecba71`  
		Last Modified: Mon, 22 Jul 2024 19:59:03 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240721.0.248532`

```console
$ docker pull archlinux@sha256:76fbb2a91a9c06b05372eb2c2e0a0edf19a864258284e2dad2002c96f776c031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:26355e4be5736c53efac48531b80d0ea1b32513e7e5d972098dd21a17cd72e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151088780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e895e05153b430a2a12984c31a25e52e9d23ab3bc71f1a314ccca1dd2171ae7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d60d5665bb190f639c1d4f286977018d4342bc47593af30e0b92968fe432d0bc`  
		Last Modified: Mon, 22 Jul 2024 19:59:06 GMT  
		Size: 151.1 MB (151080489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56de0cb20f43c946371788cf57a2e4218c3aef7c9f3b5e136296f03f54645dfb`  
		Last Modified: Mon, 22 Jul 2024 19:59:03 GMT  
		Size: 8.3 KB (8291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:73075f0609136245902753e42fecec5b3bfcbd6bc13fbc7d518eb17bd66b4955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f95a0f7c288ccfb9d74945c79034e1da3d3df3b73508815159f4b796787a5f`

```dockerfile
```

-	Layers:
	-	`sha256:29241b1b22ea97bde5a201e66a13d3fdf2048792ab418e5f03ac7f197a0a9a88`  
		Last Modified: Mon, 22 Jul 2024 19:59:04 GMT  
		Size: 8.1 MB (8098505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5030466b8633e0e22c1645a53d8de4cb31d8fb8a7026642e5e524adbbecba71`  
		Last Modified: Mon, 22 Jul 2024 19:59:03 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:904a02d4c9629b3b793dfb50db6adfeec1c6f6bcf4bc3064492190378c1645a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:992c7760458aabf9e0318cfdf78f8213afbd4d4c1e65ac47b78447a93c614246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271452604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2682e2187c9d3e15f79346917a5c6fe08ae2251e8bedddd61cdf48b2ab7df4b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:68f76d89052db3b531b4590cccff8643757330318ed8f33f844421089f752f3e`  
		Last Modified: Mon, 22 Jul 2024 19:59:19 GMT  
		Size: 271.4 MB (271443577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe652d6bc95c7768c93c69e6f102853e0cfe50b99b8cec7d467df6cd7c8acf`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:475bd249c3845413fc736cc474fe88b28c407aef6042defc5b3e3c2c3717f6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11800120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ce15d15e18d0fb6e333fde5aa2071c1f2579d64576eab5327ebcfd6576beb8`

```dockerfile
```

-	Layers:
	-	`sha256:6d96c50ff5225eab7385c54e249a93045fbd5cb95cc354d58f506c06d289f708`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 11.8 MB (11788617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93fefc2fee115f99e9851ca75e46ec703d0c2def6ebab097d680912c7eb4f285`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240721.0.248532`

```console
$ docker pull archlinux@sha256:904a02d4c9629b3b793dfb50db6adfeec1c6f6bcf4bc3064492190378c1645a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:992c7760458aabf9e0318cfdf78f8213afbd4d4c1e65ac47b78447a93c614246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271452604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2682e2187c9d3e15f79346917a5c6fe08ae2251e8bedddd61cdf48b2ab7df4b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:68f76d89052db3b531b4590cccff8643757330318ed8f33f844421089f752f3e`  
		Last Modified: Mon, 22 Jul 2024 19:59:19 GMT  
		Size: 271.4 MB (271443577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe652d6bc95c7768c93c69e6f102853e0cfe50b99b8cec7d467df6cd7c8acf`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:475bd249c3845413fc736cc474fe88b28c407aef6042defc5b3e3c2c3717f6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11800120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ce15d15e18d0fb6e333fde5aa2071c1f2579d64576eab5327ebcfd6576beb8`

```dockerfile
```

-	Layers:
	-	`sha256:6d96c50ff5225eab7385c54e249a93045fbd5cb95cc354d58f506c06d289f708`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 11.8 MB (11788617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93fefc2fee115f99e9851ca75e46ec703d0c2def6ebab097d680912c7eb4f285`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:76fbb2a91a9c06b05372eb2c2e0a0edf19a864258284e2dad2002c96f776c031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:26355e4be5736c53efac48531b80d0ea1b32513e7e5d972098dd21a17cd72e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151088780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e895e05153b430a2a12984c31a25e52e9d23ab3bc71f1a314ccca1dd2171ae7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d60d5665bb190f639c1d4f286977018d4342bc47593af30e0b92968fe432d0bc`  
		Last Modified: Mon, 22 Jul 2024 19:59:06 GMT  
		Size: 151.1 MB (151080489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56de0cb20f43c946371788cf57a2e4218c3aef7c9f3b5e136296f03f54645dfb`  
		Last Modified: Mon, 22 Jul 2024 19:59:03 GMT  
		Size: 8.3 KB (8291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:73075f0609136245902753e42fecec5b3bfcbd6bc13fbc7d518eb17bd66b4955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f95a0f7c288ccfb9d74945c79034e1da3d3df3b73508815159f4b796787a5f`

```dockerfile
```

-	Layers:
	-	`sha256:29241b1b22ea97bde5a201e66a13d3fdf2048792ab418e5f03ac7f197a0a9a88`  
		Last Modified: Mon, 22 Jul 2024 19:59:04 GMT  
		Size: 8.1 MB (8098505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5030466b8633e0e22c1645a53d8de4cb31d8fb8a7026642e5e524adbbecba71`  
		Last Modified: Mon, 22 Jul 2024 19:59:03 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:445ecfc82f497ec296ce3793b0310e0bc18013f3fd3ab8399033d5df595e1d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:2138a2444d1ce2c5b741e86cbafebc3f5635878d879a5f4dfd34fb737d0e80cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321330259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004c92c235e1b2ac1787a88c264b467db64725ed6a98027563363fba1b6533d1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:40dd90a9addf83cc89f51ca591fa1899c47712ae9d66995c5bcb684036b7f3b9`  
		Last Modified: Mon, 22 Jul 2024 19:59:36 GMT  
		Size: 321.3 MB (321320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead08b7f527112495853997c4f6e076297fafbeee4a4ff1bf40a2afd0ca6d008`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 10.2 KB (10227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:e6bd081033d4d5d84f94a11dfb2a126d62702446fd904c54d47d9ce354df56e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12067542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e9dac2e757edefc786d3b4e6108bcb7e76a331c4c9c710ff98fd42cc6d1f93`

```dockerfile
```

-	Layers:
	-	`sha256:99c4101fb50184fc9aae3e26d7520a4e08546cb5a44aa76aa19bb13fd24fe554`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 12.1 MB (12055983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec85316c8497a7c998b161253f89108c38e0fe32080efdafddf9f030e8b9a57f`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240721.0.248532`

```console
$ docker pull archlinux@sha256:445ecfc82f497ec296ce3793b0310e0bc18013f3fd3ab8399033d5df595e1d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:2138a2444d1ce2c5b741e86cbafebc3f5635878d879a5f4dfd34fb737d0e80cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321330259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004c92c235e1b2ac1787a88c264b467db64725ed6a98027563363fba1b6533d1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:40dd90a9addf83cc89f51ca591fa1899c47712ae9d66995c5bcb684036b7f3b9`  
		Last Modified: Mon, 22 Jul 2024 19:59:36 GMT  
		Size: 321.3 MB (321320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead08b7f527112495853997c4f6e076297fafbeee4a4ff1bf40a2afd0ca6d008`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 10.2 KB (10227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:e6bd081033d4d5d84f94a11dfb2a126d62702446fd904c54d47d9ce354df56e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12067542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e9dac2e757edefc786d3b4e6108bcb7e76a331c4c9c710ff98fd42cc6d1f93`

```dockerfile
```

-	Layers:
	-	`sha256:99c4101fb50184fc9aae3e26d7520a4e08546cb5a44aa76aa19bb13fd24fe554`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 12.1 MB (12055983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec85316c8497a7c998b161253f89108c38e0fe32080efdafddf9f030e8b9a57f`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.in-toto+json
