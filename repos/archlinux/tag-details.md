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
$ docker pull archlinux@sha256:a58fb33d8c7206869f7b718844ac8c849fa6a1ed811964153d33d41d096f600f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:50df1b242e2160d0d4cb7fa537e975bd2645fd7cd881a77f6e0210aea5f02587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151088755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15148a54b5fcc58f9d033bdc91d9d36a54bbb201fd202d2ff0ef79bb2f4e1f0e`
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
	-	`sha256:ad89e6a4db7258410d52ee2bf413c0ab30a2b3d955a29988cd17ec2da83a634a`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 8.3 KB (8266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:38afb58a07758e25bf1731f320aadbcdde0b32295909ecbeb9d2e0fe66cf5005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0a1b9732b6893ae31782a8d146307903a60a417b7d0713da3e062a8312bfef`

```dockerfile
```

-	Layers:
	-	`sha256:50be05d4c4748cce539e4ae26d202ada111e55183874695744f3e49ec8cdaa9f`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 8.1 MB (8098505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2d842272abbf169835e23a139787015b3f915dc85ca0b9c5466d38552014e9`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240721.0.248532`

```console
$ docker pull archlinux@sha256:a58fb33d8c7206869f7b718844ac8c849fa6a1ed811964153d33d41d096f600f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:50df1b242e2160d0d4cb7fa537e975bd2645fd7cd881a77f6e0210aea5f02587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151088755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15148a54b5fcc58f9d033bdc91d9d36a54bbb201fd202d2ff0ef79bb2f4e1f0e`
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
	-	`sha256:ad89e6a4db7258410d52ee2bf413c0ab30a2b3d955a29988cd17ec2da83a634a`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 8.3 KB (8266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:38afb58a07758e25bf1731f320aadbcdde0b32295909ecbeb9d2e0fe66cf5005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0a1b9732b6893ae31782a8d146307903a60a417b7d0713da3e062a8312bfef`

```dockerfile
```

-	Layers:
	-	`sha256:50be05d4c4748cce539e4ae26d202ada111e55183874695744f3e49ec8cdaa9f`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 8.1 MB (8098505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2d842272abbf169835e23a139787015b3f915dc85ca0b9c5466d38552014e9`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:21c96d7f815d65b5d7e87be20020bada9c60f2a7ad1a4157e8f0fa7526c755c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5a3f145cd6205f9480e180b03df29c34276d146543a627118e197f3b81ffe209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271452622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99722901cbc7ab7227f58a01e3920e2facd070a07204a4bb95db4ac3421ad372`
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
	-	`sha256:9aa8e0950a2527369de29232564ffd6829fb4699835136a272beab8dd36fe0c0`  
		Last Modified: Mon, 22 Jul 2024 23:04:04 GMT  
		Size: 9.0 KB (9045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:cb81038d56830e6f5f56889fb2d1ea026eefb881f31f9ad0233e8f60ca13e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11800120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056cb290416967da90db0bb4f478fbb3a19038d8f87e58c4348155b84665bbbd`

```dockerfile
```

-	Layers:
	-	`sha256:886b21f78ce6f4051c16ba0d171ef99403666317438d0f044c11c40cc828970b`  
		Last Modified: Mon, 22 Jul 2024 23:04:05 GMT  
		Size: 11.8 MB (11788617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6241cbbf84a34a085d0f3be97bcf9be0cfcc3e75094f3da0789fcacb3fb51a1e`  
		Last Modified: Mon, 22 Jul 2024 23:04:04 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240721.0.248532`

```console
$ docker pull archlinux@sha256:21c96d7f815d65b5d7e87be20020bada9c60f2a7ad1a4157e8f0fa7526c755c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:5a3f145cd6205f9480e180b03df29c34276d146543a627118e197f3b81ffe209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271452622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99722901cbc7ab7227f58a01e3920e2facd070a07204a4bb95db4ac3421ad372`
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
	-	`sha256:9aa8e0950a2527369de29232564ffd6829fb4699835136a272beab8dd36fe0c0`  
		Last Modified: Mon, 22 Jul 2024 23:04:04 GMT  
		Size: 9.0 KB (9045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:cb81038d56830e6f5f56889fb2d1ea026eefb881f31f9ad0233e8f60ca13e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11800120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056cb290416967da90db0bb4f478fbb3a19038d8f87e58c4348155b84665bbbd`

```dockerfile
```

-	Layers:
	-	`sha256:886b21f78ce6f4051c16ba0d171ef99403666317438d0f044c11c40cc828970b`  
		Last Modified: Mon, 22 Jul 2024 23:04:05 GMT  
		Size: 11.8 MB (11788617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6241cbbf84a34a085d0f3be97bcf9be0cfcc3e75094f3da0789fcacb3fb51a1e`  
		Last Modified: Mon, 22 Jul 2024 23:04:04 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a58fb33d8c7206869f7b718844ac8c849fa6a1ed811964153d33d41d096f600f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:50df1b242e2160d0d4cb7fa537e975bd2645fd7cd881a77f6e0210aea5f02587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151088755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15148a54b5fcc58f9d033bdc91d9d36a54bbb201fd202d2ff0ef79bb2f4e1f0e`
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
	-	`sha256:ad89e6a4db7258410d52ee2bf413c0ab30a2b3d955a29988cd17ec2da83a634a`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 8.3 KB (8266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:38afb58a07758e25bf1731f320aadbcdde0b32295909ecbeb9d2e0fe66cf5005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0a1b9732b6893ae31782a8d146307903a60a417b7d0713da3e062a8312bfef`

```dockerfile
```

-	Layers:
	-	`sha256:50be05d4c4748cce539e4ae26d202ada111e55183874695744f3e49ec8cdaa9f`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 8.1 MB (8098505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2d842272abbf169835e23a139787015b3f915dc85ca0b9c5466d38552014e9`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:1fdc4c5faac1b8cb347bd897103bd5431dae3e0e34067e131fc55f9761d6a45d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8c4d9ef0c18a8dd6238d58736a14cdef7395509a9f1e3c4100942e43ba84bbc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321330216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4735d9134311d54edc7a0e33184c5b5a45c935109fcd3cf8def03b41a57e78`
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
	-	`sha256:4d8d694a178751287b41839cfc74ba49f9a9f8083b3ce036add39135c81ab851`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:617109e53823a36fb113b8227df712806fbd4bf88598e9919dca4ff906ff2c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12067542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aab41e7a2f1266889ab885a235fb175e4b01e177f50c8821c202d0603b97504`

```dockerfile
```

-	Layers:
	-	`sha256:2bc188ca5d15e72f2f7f20772645d4f0010204ab97b03111c4d50b64388df05b`  
		Last Modified: Mon, 22 Jul 2024 23:04:27 GMT  
		Size: 12.1 MB (12055983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8edbb02df9fca5b9c02ebe20fc29550e124a479ccbba3f183bee616acf2dcf23`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240721.0.248532`

```console
$ docker pull archlinux@sha256:1fdc4c5faac1b8cb347bd897103bd5431dae3e0e34067e131fc55f9761d6a45d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:8c4d9ef0c18a8dd6238d58736a14cdef7395509a9f1e3c4100942e43ba84bbc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321330216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4735d9134311d54edc7a0e33184c5b5a45c935109fcd3cf8def03b41a57e78`
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
	-	`sha256:4d8d694a178751287b41839cfc74ba49f9a9f8083b3ce036add39135c81ab851`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:617109e53823a36fb113b8227df712806fbd4bf88598e9919dca4ff906ff2c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12067542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aab41e7a2f1266889ab885a235fb175e4b01e177f50c8821c202d0603b97504`

```dockerfile
```

-	Layers:
	-	`sha256:2bc188ca5d15e72f2f7f20772645d4f0010204ab97b03111c4d50b64388df05b`  
		Last Modified: Mon, 22 Jul 2024 23:04:27 GMT  
		Size: 12.1 MB (12055983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8edbb02df9fca5b9c02ebe20fc29550e124a479ccbba3f183bee616acf2dcf23`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.in-toto+json
