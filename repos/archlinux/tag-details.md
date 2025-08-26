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
$ docker pull archlinux@sha256:97c56e9c792dc50df96c77187255a752f479698c9beb4aa9caeb9fe4639a7590
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0ae99d31dec8d486b79831481e66be38eb384e5ae27c28929a9da1a03dbe535e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164063896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d908c4dc4a4535c266e1a68debfc16b80e51cd3582876df48bc443dd09618d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f6dbfeb25e4d5cd2e7c173987dcb74e3620311b54f906cbddb04b52d6ef1fff`  
		Last Modified: Mon, 25 Aug 2025 22:48:33 GMT  
		Size: 164.1 MB (164055570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e4b51ca8e610cc6392506347415c55a2a2491d5d2d5166d494bde2d459548`  
		Last Modified: Mon, 25 Aug 2025 19:55:33 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:6fa71df4c776e0ef083323e58dc17905f9c1bcfcab40d241f109a148b865341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d8418d52c7ab1737ef1d0d0f5f40e684104bf1dfa19efb1f9f0ed23eeda41d`

```dockerfile
```

-	Layers:
	-	`sha256:62f615734ad75439f23f74085d2e67a7570affe1a9186fb0e57a2e3027ea5530`  
		Last Modified: Mon, 25 Aug 2025 22:48:18 GMT  
		Size: 8.2 MB (8162397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9ed6f343a725a9e636432546601265ceb6d4cc9c3ae6e9f29a0d8c580717da`  
		Last Modified: Mon, 25 Aug 2025 22:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250824.0.410029`

```console
$ docker pull archlinux@sha256:97c56e9c792dc50df96c77187255a752f479698c9beb4aa9caeb9fe4639a7590
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250824.0.410029` - linux; amd64

```console
$ docker pull archlinux@sha256:0ae99d31dec8d486b79831481e66be38eb384e5ae27c28929a9da1a03dbe535e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164063896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d908c4dc4a4535c266e1a68debfc16b80e51cd3582876df48bc443dd09618d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f6dbfeb25e4d5cd2e7c173987dcb74e3620311b54f906cbddb04b52d6ef1fff`  
		Last Modified: Mon, 25 Aug 2025 22:48:33 GMT  
		Size: 164.1 MB (164055570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e4b51ca8e610cc6392506347415c55a2a2491d5d2d5166d494bde2d459548`  
		Last Modified: Mon, 25 Aug 2025 19:55:33 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250824.0.410029` - unknown; unknown

```console
$ docker pull archlinux@sha256:6fa71df4c776e0ef083323e58dc17905f9c1bcfcab40d241f109a148b865341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d8418d52c7ab1737ef1d0d0f5f40e684104bf1dfa19efb1f9f0ed23eeda41d`

```dockerfile
```

-	Layers:
	-	`sha256:62f615734ad75439f23f74085d2e67a7570affe1a9186fb0e57a2e3027ea5530`  
		Last Modified: Mon, 25 Aug 2025 22:48:18 GMT  
		Size: 8.2 MB (8162397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9ed6f343a725a9e636432546601265ceb6d4cc9c3ae6e9f29a0d8c580717da`  
		Last Modified: Mon, 25 Aug 2025 22:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:8ccc930c28ab4f483ff9bc1b53957150fbe94afe48928ebb0b14a8af41c75023
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:656656b38529210a575736bfb5eabbd835ae321c4d5b14a07a489acef3deb844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289139093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71915b2f439c1152983c3eed417c5e410b3dab02d03dca20c3628e5ecc9c5c46`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:834bd6aa009ff890ad3d3c9d51ebf96eb0dd6cd845ae62d44a5d0ad64487911d`  
		Last Modified: Mon, 25 Aug 2025 22:49:24 GMT  
		Size: 289.1 MB (289129940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8bf13b8dc24ccd7f003e7e64dfe1f1b88f271ce3222752d03edcdcaef5c3e7`  
		Last Modified: Mon, 25 Aug 2025 19:53:52 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:5381edb1ae3c1245c7fcedb94add28020d99655ec1fd046a3eb0dc57c7e136d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b76856c616da7626772ef03651e53448068ea64f40e2b49d8caf67965482fcd`

```dockerfile
```

-	Layers:
	-	`sha256:93fba30b5d942b96456fe65b3c1ff4f73275d19078c2da9c89570712e14658b2`  
		Last Modified: Mon, 25 Aug 2025 22:48:21 GMT  
		Size: 12.1 MB (12063807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59f9f676d962f92bc2559ad360890573f8d5f58acef82033acb4d95c8c4b098`  
		Last Modified: Mon, 25 Aug 2025 22:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250824.0.410029`

```console
$ docker pull archlinux@sha256:8ccc930c28ab4f483ff9bc1b53957150fbe94afe48928ebb0b14a8af41c75023
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250824.0.410029` - linux; amd64

```console
$ docker pull archlinux@sha256:656656b38529210a575736bfb5eabbd835ae321c4d5b14a07a489acef3deb844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289139093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71915b2f439c1152983c3eed417c5e410b3dab02d03dca20c3628e5ecc9c5c46`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:834bd6aa009ff890ad3d3c9d51ebf96eb0dd6cd845ae62d44a5d0ad64487911d`  
		Last Modified: Mon, 25 Aug 2025 22:49:24 GMT  
		Size: 289.1 MB (289129940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8bf13b8dc24ccd7f003e7e64dfe1f1b88f271ce3222752d03edcdcaef5c3e7`  
		Last Modified: Mon, 25 Aug 2025 19:53:52 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250824.0.410029` - unknown; unknown

```console
$ docker pull archlinux@sha256:5381edb1ae3c1245c7fcedb94add28020d99655ec1fd046a3eb0dc57c7e136d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b76856c616da7626772ef03651e53448068ea64f40e2b49d8caf67965482fcd`

```dockerfile
```

-	Layers:
	-	`sha256:93fba30b5d942b96456fe65b3c1ff4f73275d19078c2da9c89570712e14658b2`  
		Last Modified: Mon, 25 Aug 2025 22:48:21 GMT  
		Size: 12.1 MB (12063807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59f9f676d962f92bc2559ad360890573f8d5f58acef82033acb4d95c8c4b098`  
		Last Modified: Mon, 25 Aug 2025 22:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:97c56e9c792dc50df96c77187255a752f479698c9beb4aa9caeb9fe4639a7590
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0ae99d31dec8d486b79831481e66be38eb384e5ae27c28929a9da1a03dbe535e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164063896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d908c4dc4a4535c266e1a68debfc16b80e51cd3582876df48bc443dd09618d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f6dbfeb25e4d5cd2e7c173987dcb74e3620311b54f906cbddb04b52d6ef1fff`  
		Last Modified: Mon, 25 Aug 2025 22:48:33 GMT  
		Size: 164.1 MB (164055570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e4b51ca8e610cc6392506347415c55a2a2491d5d2d5166d494bde2d459548`  
		Last Modified: Mon, 25 Aug 2025 19:55:33 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:6fa71df4c776e0ef083323e58dc17905f9c1bcfcab40d241f109a148b865341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d8418d52c7ab1737ef1d0d0f5f40e684104bf1dfa19efb1f9f0ed23eeda41d`

```dockerfile
```

-	Layers:
	-	`sha256:62f615734ad75439f23f74085d2e67a7570affe1a9186fb0e57a2e3027ea5530`  
		Last Modified: Mon, 25 Aug 2025 22:48:18 GMT  
		Size: 8.2 MB (8162397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9ed6f343a725a9e636432546601265ceb6d4cc9c3ae6e9f29a0d8c580717da`  
		Last Modified: Mon, 25 Aug 2025 22:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:382026febe9d0647082ecc0004aee156bdc8b571d8ff427d9dbb4b7a7f7f52c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:dc4817e2db60ecb6ad8ba795d6e292ea003d0caa83fd5bf309a847145334c8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340455063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06393749d4c9af90d7870c757bb1f227addde5e2aa079a00d142dfd9de82b739`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a18a861ef7fafe9556993468d877ce370d9029dfd521ac9f6e65ed986e505cf6`  
		Last Modified: Mon, 25 Aug 2025 23:31:18 GMT  
		Size: 340.4 MB (340444765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022e18f0432d86e9257f25999b3cfc3b6edce6537d7f35e4c7c0fc2d4acf9ff`  
		Last Modified: Mon, 25 Aug 2025 19:54:04 GMT  
		Size: 10.3 KB (10298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:fb60cd6ff4e3b67a47eb9e99ae9405759666babec479a0abf483ae22b73ff418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12344511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c536f1e8d7954b1ccb2156e8629904bcff0a986f6fbef851fa122fb7bea2605`

```dockerfile
```

-	Layers:
	-	`sha256:95c826324f897edf831dd6b29b3f9b79526319e26fac7b6675aed6d8f026cc49`  
		Last Modified: Mon, 25 Aug 2025 22:48:27 GMT  
		Size: 12.3 MB (12332701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f67b9447269510a2ba67ca37df865df646c31c25c714783a834c1ac9b3fc40`  
		Last Modified: Mon, 25 Aug 2025 22:48:28 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250824.0.410029`

```console
$ docker pull archlinux@sha256:382026febe9d0647082ecc0004aee156bdc8b571d8ff427d9dbb4b7a7f7f52c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250824.0.410029` - linux; amd64

```console
$ docker pull archlinux@sha256:dc4817e2db60ecb6ad8ba795d6e292ea003d0caa83fd5bf309a847145334c8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340455063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06393749d4c9af90d7870c757bb1f227addde5e2aa079a00d142dfd9de82b739`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a18a861ef7fafe9556993468d877ce370d9029dfd521ac9f6e65ed986e505cf6`  
		Last Modified: Mon, 25 Aug 2025 23:31:18 GMT  
		Size: 340.4 MB (340444765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022e18f0432d86e9257f25999b3cfc3b6edce6537d7f35e4c7c0fc2d4acf9ff`  
		Last Modified: Mon, 25 Aug 2025 19:54:04 GMT  
		Size: 10.3 KB (10298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250824.0.410029` - unknown; unknown

```console
$ docker pull archlinux@sha256:fb60cd6ff4e3b67a47eb9e99ae9405759666babec479a0abf483ae22b73ff418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12344511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c536f1e8d7954b1ccb2156e8629904bcff0a986f6fbef851fa122fb7bea2605`

```dockerfile
```

-	Layers:
	-	`sha256:95c826324f897edf831dd6b29b3f9b79526319e26fac7b6675aed6d8f026cc49`  
		Last Modified: Mon, 25 Aug 2025 22:48:27 GMT  
		Size: 12.3 MB (12332701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f67b9447269510a2ba67ca37df865df646c31c25c714783a834c1ac9b3fc40`  
		Last Modified: Mon, 25 Aug 2025 22:48:28 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
