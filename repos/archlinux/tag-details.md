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
$ docker pull archlinux@sha256:c136b06a4f786b84c1cc0d2494fabdf9be8811d15051cd4404deb5c3dc0b2e57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:34c848de96e5e94268710ef1b520acd7e6cd9ae49b77a62aaa28b9bcc0a38552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165329516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60cf1d6ee7e10c450ee32d39393589a76e84ad9f3c55e0a12c59d8a4b08a980`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.version=20251019.0.436919
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.created=2025-10-19T00:07:20+00:00
# Sun, 19 Oct 2025 00:07:20 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251019.0.436919' /etc/os-release # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
ENV LANG=C.UTF-8
# Sun, 19 Oct 2025 00:07:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a59b1e251b8568aff85b2ffb74ea2f9ed87fee3de7c0b9b3940b6ce56c9c7c13`  
		Last Modified: Mon, 20 Oct 2025 21:29:18 GMT  
		Size: 165.3 MB (165321179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b0775ea0f9481add0c91f4644ee5834b792b6aa0babf5e465a3574fe8c33a`  
		Last Modified: Mon, 20 Oct 2025 20:27:15 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:702233454069087682ba2484f6b71d8f5b6dc53bc5c6ddb5527812d3de218bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea91b6c1f070904eb2fc7f471a38e5ea9006153d0ccef14ac0e9787eb4667a3`

```dockerfile
```

-	Layers:
	-	`sha256:b0646ee5ed692207731c857b9ff1974741162fbbe56da1cb2756920f60aca691`  
		Last Modified: Mon, 20 Oct 2025 22:48:15 GMT  
		Size: 8.2 MB (8217645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c8b795adf8dede24ac62d32dcbddb0f637870b3afe6744b6d5d2bcc5e60faa`  
		Last Modified: Mon, 20 Oct 2025 22:48:16 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251214.0.467559`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:943bdad9e9d0d23503f24797b44ce2cc1531bf101e18b3e7fb8c8776190dc45e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:45507a3dd4b47f79e989d8f5c68f2a3ac4e7762ae02df1a9021079d46b31f8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290408468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cea3620a76cfbe078484b4e01d03e3fd3640a589136415e91779fa1004864ce`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.version=20251019.0.436919
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.created=2025-10-19T00:07:20+00:00
# Sun, 19 Oct 2025 00:07:20 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251019.0.436919' /etc/os-release # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
ENV LANG=C.UTF-8
# Sun, 19 Oct 2025 00:07:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cf8eef8fdeb239bae8999d4e9016b367fd988645bc52e776cbf8b67ba86ca707`  
		Last Modified: Mon, 20 Oct 2025 22:50:29 GMT  
		Size: 290.4 MB (290399321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe63a10669129fcee9af6efb2bc0327e857aa6ba4510d960ca467c3493283cbd`  
		Last Modified: Mon, 20 Oct 2025 20:27:15 GMT  
		Size: 9.1 KB (9147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:1e04511da147209b36c93b070f72a58d7df620f98379b55a53ae8d1cf6304254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad73e5c8de29c9643e69ce0da9ebdd3b8cba9f7240da6fc79e1a47b701ca9255`

```dockerfile
```

-	Layers:
	-	`sha256:885961d144eb276f2ef524a9c5e8659f0490e9041c6df8b4fb82e5724eda3a4d`  
		Last Modified: Mon, 20 Oct 2025 22:48:23 GMT  
		Size: 12.1 MB (12118981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47f78177bbbf877c7b57b597469b7b380326943486c084abd64cfe0961eed410`  
		Last Modified: Mon, 20 Oct 2025 22:48:23 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251214.0.467559`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:c136b06a4f786b84c1cc0d2494fabdf9be8811d15051cd4404deb5c3dc0b2e57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:34c848de96e5e94268710ef1b520acd7e6cd9ae49b77a62aaa28b9bcc0a38552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165329516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60cf1d6ee7e10c450ee32d39393589a76e84ad9f3c55e0a12c59d8a4b08a980`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.version=20251019.0.436919
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.created=2025-10-19T00:07:20+00:00
# Sun, 19 Oct 2025 00:07:20 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251019.0.436919' /etc/os-release # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
ENV LANG=C.UTF-8
# Sun, 19 Oct 2025 00:07:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a59b1e251b8568aff85b2ffb74ea2f9ed87fee3de7c0b9b3940b6ce56c9c7c13`  
		Last Modified: Mon, 20 Oct 2025 21:29:18 GMT  
		Size: 165.3 MB (165321179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b0775ea0f9481add0c91f4644ee5834b792b6aa0babf5e465a3574fe8c33a`  
		Last Modified: Mon, 20 Oct 2025 20:27:15 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:702233454069087682ba2484f6b71d8f5b6dc53bc5c6ddb5527812d3de218bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea91b6c1f070904eb2fc7f471a38e5ea9006153d0ccef14ac0e9787eb4667a3`

```dockerfile
```

-	Layers:
	-	`sha256:b0646ee5ed692207731c857b9ff1974741162fbbe56da1cb2756920f60aca691`  
		Last Modified: Mon, 20 Oct 2025 22:48:15 GMT  
		Size: 8.2 MB (8217645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c8b795adf8dede24ac62d32dcbddb0f637870b3afe6744b6d5d2bcc5e60faa`  
		Last Modified: Mon, 20 Oct 2025 22:48:16 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:c52936673f184d8c3bdcebd4fc6d5403514bc18e175d26fa7c3793b72cbb1d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:44e30138991d38036d0894982230cd74588aa5569e568493c85c1ab7d434d8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341725875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f53020a3b2fce039f6cbadb7aec91cb6c9c83ca993c5d126a5b5f643094addb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.version=20251019.0.436919
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.created=2025-10-19T00:07:20+00:00
# Sun, 19 Oct 2025 00:07:20 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251019.0.436919' /etc/os-release # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
ENV LANG=C.UTF-8
# Sun, 19 Oct 2025 00:07:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a43e711e3fbd4e30e7a99e9ce907fb06f984d509678fa60f3ca9fc42598baa7f`  
		Last Modified: Mon, 20 Oct 2025 22:56:53 GMT  
		Size: 341.7 MB (341715623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf121b786352eeee330d472642e8989ff20bceafcadb1623704f11275a118a0`  
		Last Modified: Mon, 20 Oct 2025 20:27:50 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a295df9d8b1b9b58bcdd6f54e79f6212fd3412dacac22e41a5e7dbdd60d25b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12399580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934cf46797d3d466de5f1403ff14c1c4cc600d260c5f93bf68d55277e47e17da`

```dockerfile
```

-	Layers:
	-	`sha256:258189b3f3b436f10e31bf58372d8fb45c6a4c8d1cd6289d15e335dd2129aa5e`  
		Last Modified: Mon, 20 Oct 2025 22:48:29 GMT  
		Size: 12.4 MB (12387769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3430635cf28312485efb75431807ca09f28f462ecd8eabec6624433bdba2d19e`  
		Last Modified: Mon, 20 Oct 2025 22:48:30 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251214.0.467559`

**does not exist** (yet?)
