<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240818.0.255804`](#archlinuxbase-202408180255804)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240818.0.255804`](#archlinuxbase-devel-202408180255804)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240818.0.255804`](#archlinuxmultilib-devel-202408180255804)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:271083843fa6569f02dfc78b2bab94fce8d705c8aa9d581fc838437930ed977b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9ce68291a5781e56550e15a02a17d1b96f0ec27a3868b9db497b35999876afb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151159668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475d1d5e29bed7d90cbc70f34b8da466f942d649bdf21d3f28c45e96124d166`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20240811.0.253648
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-08-11T00:07:52+00:00
# Sun, 11 Aug 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240811.0.253648' /etc/os-release # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 11 Aug 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:41b97f57fdb9eda7d32a74c17046812257d854ea5fc34380b033a53f66b80190`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 151.2 MB (151151362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eff8d7dad74c783bba3d3e4f5c92ffd8353c6167149683f41670239942a3e52`  
		Last Modified: Mon, 12 Aug 2024 16:56:29 GMT  
		Size: 8.3 KB (8306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:98969c9c385675332f7db299be43a7276a2726f32474561b3508156f657b098d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d7e2b0beaf1a1649c859c1a21e7a92add0cd8263d9f962bb89b549d5dbbd2e`

```dockerfile
```

-	Layers:
	-	`sha256:59e2c175a479dcb6e2f89efe40e5fb53adae76e41a4f296c3c8245d40e78a76b`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 8.1 MB (8103929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96baec7823e60d53894e6d9920ded7076830ac276a86fea35a85d99dd75dfafb`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240818.0.255804`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:85386aeb0b8b40b2aa306056c1d9c8827356cfd9b5d74ae159092d46a0a6a4b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d703d0c3d9c2b43c45d685c61a630a3fb6b434bdaf92f4ff3b1fa6a19ce9fa38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271722146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bb71975f3172ab5edcfa81715b2583b3a3e6d7e029bcf509b8ac25b4c52832`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20240811.0.253648
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-08-11T00:07:52+00:00
# Sun, 11 Aug 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240811.0.253648' /etc/os-release # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 11 Aug 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8f5ad95fba3c70fdb088c4d4dece0a1ffccd67e67c78a7ea0c15051628382041`  
		Last Modified: Mon, 12 Aug 2024 16:57:04 GMT  
		Size: 271.7 MB (271713096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057791028ae05dcb6e7c4030c6492f3fc12a183a81f36a8c8b75e1bc3d69ced0`  
		Last Modified: Mon, 12 Aug 2024 16:57:00 GMT  
		Size: 9.1 KB (9050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2375f7922dfeca8b3d63beb27436f8bcdc3da08aa71b8c1db5651404f3dfd3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848ad116af6813b4c1dc71479281d8a646ced7992f6e1b114ca1f80ceb7f2bcd`

```dockerfile
```

-	Layers:
	-	`sha256:468170ebc267371f1741132b2b6d225e468cbfbf555cd0a68829fc806c7434ab`  
		Last Modified: Mon, 12 Aug 2024 16:57:00 GMT  
		Size: 11.8 MB (11818138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c668b256c4301ef947eb69ca00450c8fe9e2f8077d9f115078bcf9fd33e047`  
		Last Modified: Mon, 12 Aug 2024 16:57:00 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240818.0.255804`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:271083843fa6569f02dfc78b2bab94fce8d705c8aa9d581fc838437930ed977b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9ce68291a5781e56550e15a02a17d1b96f0ec27a3868b9db497b35999876afb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151159668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475d1d5e29bed7d90cbc70f34b8da466f942d649bdf21d3f28c45e96124d166`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20240811.0.253648
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-08-11T00:07:52+00:00
# Sun, 11 Aug 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240811.0.253648' /etc/os-release # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 11 Aug 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:41b97f57fdb9eda7d32a74c17046812257d854ea5fc34380b033a53f66b80190`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 151.2 MB (151151362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eff8d7dad74c783bba3d3e4f5c92ffd8353c6167149683f41670239942a3e52`  
		Last Modified: Mon, 12 Aug 2024 16:56:29 GMT  
		Size: 8.3 KB (8306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:98969c9c385675332f7db299be43a7276a2726f32474561b3508156f657b098d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d7e2b0beaf1a1649c859c1a21e7a92add0cd8263d9f962bb89b549d5dbbd2e`

```dockerfile
```

-	Layers:
	-	`sha256:59e2c175a479dcb6e2f89efe40e5fb53adae76e41a4f296c3c8245d40e78a76b`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 8.1 MB (8103929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96baec7823e60d53894e6d9920ded7076830ac276a86fea35a85d99dd75dfafb`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:5aa722de8945fa66550498935a47cd82eb500d1b77c7e93e9d27109704923eb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:43406cf54cac37988bce93ad3da51193b7d5aed9b770d1f5a514759983e52dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321618527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d75688e4843e6be26eac02cbbb379da2ba1fbfc8056b25365207c23bdd0083`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20240811.0.253648
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-08-11T00:07:52+00:00
# Sun, 11 Aug 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240811.0.253648' /etc/os-release # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 11 Aug 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f58303c2dafef45f1aae7aeb62afc703cee59842d9290051b70b6b85bff175da`  
		Last Modified: Mon, 12 Aug 2024 16:57:17 GMT  
		Size: 321.6 MB (321608337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f69d045dd51ec19952ad9dd37480cf3e58afee258a413c342a51a0d959b7f`  
		Last Modified: Mon, 12 Aug 2024 16:57:12 GMT  
		Size: 10.2 KB (10190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3c4f44b741b296170f8cc4c3f1177b007ec0c297d27971afa5e7b130e9a805fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d8ee0b964342b4be44f4dfa7083540490819118326f03a915a7342e974caf7`

```dockerfile
```

-	Layers:
	-	`sha256:4694a60ac3904dbc05e3dcc03ef09ebbc4b80273f1d57236577ff4772ce2f480`  
		Last Modified: Mon, 12 Aug 2024 16:57:13 GMT  
		Size: 12.1 MB (12085504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b59507ebfb5d379421cd9016fc2a44d7c95960df53a00a31b5e7e19f850916bf`  
		Last Modified: Mon, 12 Aug 2024 16:57:12 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240818.0.255804`

**does not exist** (yet?)
