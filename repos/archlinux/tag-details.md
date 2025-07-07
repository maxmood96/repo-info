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
$ docker pull archlinux@sha256:6e644b0d7ac1543ce6368d0cd9f919d6d234c718a721fdabd132f50acb0488b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a4c7712b66d585875f0be4142c5d3c887e6d7019bfeacf4e94029e0fe8b699a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163111770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec71e82971c8667f8b5cb241f1b2c3514fd064f66befd23d8524368491081e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250629.0.373469
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-06-29T00:07:42+00:00
# Sun, 29 Jun 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250629.0.373469' /etc/os-release # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 29 Jun 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2f578d9f91c18debeca37b4769108ce6e35f0a710925f5fa19ecf9889f11c4ce`  
		Last Modified: Mon, 30 Jun 2025 19:48:31 GMT  
		Size: 163.1 MB (163103421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d077b0b504141872c70903b2149b792faa92bb7bb2e9ffebb539c512551ad6`  
		Last Modified: Mon, 30 Jun 2025 17:16:55 GMT  
		Size: 8.3 KB (8349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:b1a212278c38a4a8042abf74a057f8d04ca1cd819643b66ea4da9a5e49dc1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b38ca8c68e371545f2ac1f4c141419af3545d3936e2554239dfddd019a8bde`

```dockerfile
```

-	Layers:
	-	`sha256:e5128ee3b0fd26bf4ae9323998cd3706fbf0b35789e9d2881f061d4f9a2fd13b`  
		Last Modified: Mon, 30 Jun 2025 19:48:17 GMT  
		Size: 8.1 MB (8148784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3987e9a59d25f715feb895a5cbbbfa1244ef106e34c7cb6ddcbcbc6340a40057`  
		Last Modified: Mon, 30 Jun 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250706.0.377547`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:16c85e56b0758a09815b39463a9bc2bbc870b2599c479ef947a2824281ca500c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f2d006725e76c1bda4bf675b9ae18013ef016436a803205c5ec12e9a7d7ce919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287795686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdd57aff9175c80d61aaf62d4c588048ad8037d5c602145b6f86760471a5a0c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250629.0.373469
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-06-29T00:07:42+00:00
# Sun, 29 Jun 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250629.0.373469' /etc/os-release # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 29 Jun 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ee5dff51893a25e6219969818aad60db02458d95032d1202c08ff1d96fb75630`  
		Last Modified: Mon, 30 Jun 2025 19:48:47 GMT  
		Size: 287.8 MB (287786527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e875a54ba2950610689aa075c30f55c0cfee42d2c2285e0d2ac120b9c9ed73`  
		Last Modified: Mon, 30 Jun 2025 17:17:34 GMT  
		Size: 9.2 KB (9159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:9291d40a1b644810c3990b1a2305d037476d02116cfa22e43441b1470ccc007c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12022005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb04097676ff2776f38fd790b4d73299958b3a88efda7ed604aa7ee2c7459d1c`

```dockerfile
```

-	Layers:
	-	`sha256:d06d076ded6a16ef432cd3a7f7705791aa26014f900544759263e4959f119939`  
		Last Modified: Mon, 30 Jun 2025 19:48:21 GMT  
		Size: 12.0 MB (12010251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f663588b265114c0fda38f02170232bbf8a6d44b0bb0156cfeff37d2e581d0`  
		Last Modified: Mon, 30 Jun 2025 19:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250706.0.377547`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:6e644b0d7ac1543ce6368d0cd9f919d6d234c718a721fdabd132f50acb0488b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:a4c7712b66d585875f0be4142c5d3c887e6d7019bfeacf4e94029e0fe8b699a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163111770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec71e82971c8667f8b5cb241f1b2c3514fd064f66befd23d8524368491081e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250629.0.373469
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-06-29T00:07:42+00:00
# Sun, 29 Jun 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250629.0.373469' /etc/os-release # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 29 Jun 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2f578d9f91c18debeca37b4769108ce6e35f0a710925f5fa19ecf9889f11c4ce`  
		Last Modified: Mon, 30 Jun 2025 19:48:31 GMT  
		Size: 163.1 MB (163103421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d077b0b504141872c70903b2149b792faa92bb7bb2e9ffebb539c512551ad6`  
		Last Modified: Mon, 30 Jun 2025 17:16:55 GMT  
		Size: 8.3 KB (8349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:b1a212278c38a4a8042abf74a057f8d04ca1cd819643b66ea4da9a5e49dc1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b38ca8c68e371545f2ac1f4c141419af3545d3936e2554239dfddd019a8bde`

```dockerfile
```

-	Layers:
	-	`sha256:e5128ee3b0fd26bf4ae9323998cd3706fbf0b35789e9d2881f061d4f9a2fd13b`  
		Last Modified: Mon, 30 Jun 2025 19:48:17 GMT  
		Size: 8.1 MB (8148784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3987e9a59d25f715feb895a5cbbbfa1244ef106e34c7cb6ddcbcbc6340a40057`  
		Last Modified: Mon, 30 Jun 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:2898517074c8894a121e3d31abd8b53e4d2db3860dc65b65090bb3676fa76d69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:143d404abb92f57ab35eba564f6e82f6985310aa6bebbb260c6d6ea3b47bcc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338952093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0086058769539afa8b0b5268270995457b03c08a6969e8e25fda269cd345225`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250629.0.373469
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-06-29T00:07:42+00:00
# Sun, 29 Jun 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250629.0.373469' /etc/os-release # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 29 Jun 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b7495dd7e7362f16e7984d450d18e86d1828969cbf83c12c7bf463e6f9c65f41`  
		Last Modified: Mon, 30 Jun 2025 20:07:31 GMT  
		Size: 338.9 MB (338941824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b88b1aa8688a12df44810e87e48833d28c4d76fb5efcb289d4a1ba5e3f9b0f3`  
		Last Modified: Mon, 30 Jun 2025 17:17:53 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:85f673e640516f266a6d75bee1930c9173890e41202bbf8a8c6d203925a9125d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12290950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60ec85a0384ddab020a1f56f5553bcd72a804db6426cb2d93480d18801a0300`

```dockerfile
```

-	Layers:
	-	`sha256:4c52e50b7e8a55a45b5a66f25005c1bc224c9723d8afa0b6db44cac3ac74f7ea`  
		Last Modified: Mon, 30 Jun 2025 19:48:27 GMT  
		Size: 12.3 MB (12279140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da321d6a9913d67f6a952b330e436a30aa2a459ecedaa3d681d733eec44905e`  
		Last Modified: Mon, 30 Jun 2025 19:48:28 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250706.0.377547`

**does not exist** (yet?)
