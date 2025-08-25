<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250824.0.410029`](#archlinuxbase-202508240410029)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250824.0.410029`](#archlinuxbase-devel-202508240410029)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250824.0.410029`](#archlinuxmultilib-devel-202508240410029)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:31f0749bdb81517dc8f379feac0a3860b097f1da1f53c8315c1bae0817d6c0a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0be14bde0c8440623e0d462edb6e2df6413427ca683b2e7b5626500fc5a546d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164036524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a58446590e80db33dfa502f12009b1c6f8fe51855d9c48fa7faad773012965`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.version=20250817.0.405639
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.created=2025-08-17T00:07:25+00:00
# Sun, 17 Aug 2025 00:07:25 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250817.0.405639' /etc/os-release # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
ENV LANG=C.UTF-8
# Sun, 17 Aug 2025 00:07:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1fd63ae9298856f3b10f29e943cea5781133698ac97592190c7204d3597b97bb`  
		Last Modified: Mon, 18 Aug 2025 19:48:31 GMT  
		Size: 164.0 MB (164028195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83c0355d77e05e0698b16b3ebd7f670bd8eca71629762d5109aae566acce659`  
		Last Modified: Mon, 18 Aug 2025 16:53:48 GMT  
		Size: 8.3 KB (8329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:65b18e153c49e1af30484d2a181d97c33b9856bec4abfda54ebdb753e23dd497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33df378657b01b9c1b8ac5234d9ee99eea5a6a63ec95e0c6d12c604af7261992`

```dockerfile
```

-	Layers:
	-	`sha256:6a884fccb7886b399e64f6a774983b6548bbbc4d909ea024f4d78bc803fa7ffc`  
		Last Modified: Mon, 18 Aug 2025 19:48:21 GMT  
		Size: 8.2 MB (8162397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e020a92a579c76e2798d5d886a2d23b826187f3529fe71d8962bf5b4562782`  
		Last Modified: Mon, 18 Aug 2025 19:48:22 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250824.0.410029`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:925a18f3b29708f2e9b7850c58a71b65f36cbcaddc8e5f1ba3a77057b9bdb88e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:985d1236e051b95d80e20755349061919ca0349925c2caacdaace92d2991d5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92845b5741df93ac770a34717e57613b3d2c3d1e571456119b7b2eac2210a946`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.version=20250817.0.405639
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.created=2025-08-17T00:07:25+00:00
# Sun, 17 Aug 2025 00:07:25 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250817.0.405639' /etc/os-release # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
ENV LANG=C.UTF-8
# Sun, 17 Aug 2025 00:07:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:06a1f21ad0ba1fa6a4658ca8f40bebce6a25dc164953f4315389efc6704cbe3f`  
		Last Modified: Mon, 18 Aug 2025 19:50:18 GMT  
		Size: 289.1 MB (289118842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd76bccf9cb696f47f05a25b6df108f9826f8ad738a740be6a7baf5c3fd3a222`  
		Last Modified: Mon, 18 Aug 2025 16:54:53 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:7016575e94761e34c1def92921e37b33b38a09b56197ae1dbfca8a94414b9649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cbc1d27eb10e72f2654c2dcc1f6e7eae46e1e34b79f76d4bc73114199020b5`

```dockerfile
```

-	Layers:
	-	`sha256:0ab47556f945a32b9880aa4d76995465a9c8367b4585ad4ca5a117883cb63adb`  
		Last Modified: Mon, 18 Aug 2025 19:48:21 GMT  
		Size: 12.1 MB (12063807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2015cfd4cc960e8b811a0e00c77f9f00f3e41b9f46537e8a49be274723d30b`  
		Last Modified: Mon, 18 Aug 2025 19:48:23 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250824.0.410029`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:31f0749bdb81517dc8f379feac0a3860b097f1da1f53c8315c1bae0817d6c0a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0be14bde0c8440623e0d462edb6e2df6413427ca683b2e7b5626500fc5a546d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164036524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a58446590e80db33dfa502f12009b1c6f8fe51855d9c48fa7faad773012965`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.version=20250817.0.405639
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.created=2025-08-17T00:07:25+00:00
# Sun, 17 Aug 2025 00:07:25 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250817.0.405639' /etc/os-release # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
ENV LANG=C.UTF-8
# Sun, 17 Aug 2025 00:07:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1fd63ae9298856f3b10f29e943cea5781133698ac97592190c7204d3597b97bb`  
		Last Modified: Mon, 18 Aug 2025 19:48:31 GMT  
		Size: 164.0 MB (164028195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83c0355d77e05e0698b16b3ebd7f670bd8eca71629762d5109aae566acce659`  
		Last Modified: Mon, 18 Aug 2025 16:53:48 GMT  
		Size: 8.3 KB (8329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:65b18e153c49e1af30484d2a181d97c33b9856bec4abfda54ebdb753e23dd497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33df378657b01b9c1b8ac5234d9ee99eea5a6a63ec95e0c6d12c604af7261992`

```dockerfile
```

-	Layers:
	-	`sha256:6a884fccb7886b399e64f6a774983b6548bbbc4d909ea024f4d78bc803fa7ffc`  
		Last Modified: Mon, 18 Aug 2025 19:48:21 GMT  
		Size: 8.2 MB (8162397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e020a92a579c76e2798d5d886a2d23b826187f3529fe71d8962bf5b4562782`  
		Last Modified: Mon, 18 Aug 2025 19:48:22 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:10f14c98fb1a3476d89db888e853eb5259adec84caa5eb485316a318ba534833
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:17f7931d409b49b29da5486ba061cae7b88b2fb3703591c69fe39d437123a35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340447562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584e670b4e0b5660d130d2d52b65105d3a7f7c2b096ad8b0754db3e4b1a9f2a9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.version=20250817.0.405639
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.created=2025-08-17T00:07:25+00:00
# Sun, 17 Aug 2025 00:07:25 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250817.0.405639' /etc/os-release # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
ENV LANG=C.UTF-8
# Sun, 17 Aug 2025 00:07:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1f2b41bf42c3a563055da325cf677ade819fecdde00b8981ef0f240a7a68daf4`  
		Last Modified: Mon, 18 Aug 2025 17:09:13 GMT  
		Size: 340.4 MB (340437287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195cfba426c73771598e59b62a71a5d342cdc662606b8444df994f12b22d7e01`  
		Last Modified: Mon, 18 Aug 2025 16:55:09 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:70a921b5e4fa55e79d8c7518aaa8bce88869376e51298e43e3f4a587c704c3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12344512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8368a2b68ba64bf308c897baf8fbb432f26706d862cde29164fd8b137acb5393`

```dockerfile
```

-	Layers:
	-	`sha256:9d95aa728609f34ed9d726672de45c161d1f380a9b22e5b9bc424c1eb2b45b74`  
		Last Modified: Mon, 18 Aug 2025 19:48:27 GMT  
		Size: 12.3 MB (12332701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d95c675b5cfe267be978d766b6900a7100c4289c361ee188bc44266a7216981`  
		Last Modified: Mon, 18 Aug 2025 19:48:27 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250824.0.410029`

**does not exist** (yet?)
