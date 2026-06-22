<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260621.0.546891`](#archlinuxbase-202606210546891)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260621.0.546891`](#archlinuxbase-devel-202606210546891)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260621.0.546891`](#archlinuxmultilib-devel-202606210546891)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:ff410a88e200b133e577f5730b7bfa324e26a333075ee056bf45e911c6ac5671
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:87465c3afdaede91333d4a9239d6a1ba7f47b2ec74b376e0070e81c25e7e3ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131323041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2ba0cdeb07d0a0942e1a6902f35add9b2cc629c67dd427b4b6edcd27c996eb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.version=20260614.0.544538
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.created=2026-06-14T00:09:34+00:00
# Mon, 15 Jun 2026 18:37:44 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Jun 2026 18:37:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260614.0.544538' /etc/os-release # buildkit
# Mon, 15 Jun 2026 18:37:46 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jun 2026 18:37:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cee022eb541796c460f6eb7cebb37abbee6b1fb5203f3263c04b9e8b191f6382`  
		Last Modified: Mon, 15 Jun 2026 18:38:12 GMT  
		Size: 131.3 MB (131314369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dd4767aea960be8ddd0ae80c18a5ccc94a6a7c0702637ea3e5adbf05f455fd`  
		Last Modified: Mon, 15 Jun 2026 18:38:08 GMT  
		Size: 8.7 KB (8672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:c226da522fbf7f9dbcfeeb7ed5ba578611febd5d660851faf8db4c2c0d29284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e34d5bfe7c3253fd115de860a3fc2451af1c5a25c32d19cf2562f50e91047a`

```dockerfile
```

-	Layers:
	-	`sha256:4d2e96d3c7680cd6abae8fbb5afde28134cb2b7594c42155cc33f5357db6e758`  
		Last Modified: Mon, 15 Jun 2026 18:38:09 GMT  
		Size: 8.2 MB (8182421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b778afffd5f4220306eee62b9d341a3c9c43b5b9780735591d0b617da2535366`  
		Last Modified: Mon, 15 Jun 2026 18:38:08 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260621.0.546891`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0cf5eb78f8c3ddcdd7ccc3f9168328fb57ec6be0f83f501a0b2006590e0c92ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:9f859aff8a280ca9fd04eb493229216bf38aa7d5ab7f0a8da5eae2885a20d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303370848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afeaeb37cbe13985fabab768e31358a1c7b09d741d09f12ed32ac9f1568fa70`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.version=20260614.0.544538
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 15 Jun 2026 18:39:34 GMT
LABEL org.opencontainers.image.created=2026-06-14T00:09:34+00:00
# Mon, 15 Jun 2026 18:39:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Jun 2026 18:39:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260614.0.544538' /etc/os-release # buildkit
# Mon, 15 Jun 2026 18:39:41 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jun 2026 18:39:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d0e821d2e92139b70424f0af216f4ed56ce678c90db4835d7022c7c8fb46b266`  
		Last Modified: Mon, 15 Jun 2026 18:40:36 GMT  
		Size: 303.4 MB (303359441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d899506f0105cb067bf94d4bc4fdee5372012ed2139d2508497c9561226be7d6`  
		Last Modified: Mon, 15 Jun 2026 18:40:30 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:9d3c2dd314d40bc45bceeb1bdfbc45e36ec1f3785e7f166e7a87ec61158f7b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14397839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f65127bb6eca80a62fb048537dc1ea11b1ce19eb91d6c6bc531142eb3c4ebf`

```dockerfile
```

-	Layers:
	-	`sha256:2e4f559095ece592ffcf48f67286144b5a3f94ca29e6480d4cbbef5a89292fed`  
		Last Modified: Mon, 15 Jun 2026 18:40:31 GMT  
		Size: 14.4 MB (14386127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293a64317b1535e3d614b7a2c689143d67d18f157179ca2ebf4ec4efc1ba4121`  
		Last Modified: Mon, 15 Jun 2026 18:40:30 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260621.0.546891`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:ff410a88e200b133e577f5730b7bfa324e26a333075ee056bf45e911c6ac5671
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:87465c3afdaede91333d4a9239d6a1ba7f47b2ec74b376e0070e81c25e7e3ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131323041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2ba0cdeb07d0a0942e1a6902f35add9b2cc629c67dd427b4b6edcd27c996eb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.version=20260614.0.544538
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 15 Jun 2026 18:37:44 GMT
LABEL org.opencontainers.image.created=2026-06-14T00:09:34+00:00
# Mon, 15 Jun 2026 18:37:44 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Jun 2026 18:37:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260614.0.544538' /etc/os-release # buildkit
# Mon, 15 Jun 2026 18:37:46 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jun 2026 18:37:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cee022eb541796c460f6eb7cebb37abbee6b1fb5203f3263c04b9e8b191f6382`  
		Last Modified: Mon, 15 Jun 2026 18:38:12 GMT  
		Size: 131.3 MB (131314369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dd4767aea960be8ddd0ae80c18a5ccc94a6a7c0702637ea3e5adbf05f455fd`  
		Last Modified: Mon, 15 Jun 2026 18:38:08 GMT  
		Size: 8.7 KB (8672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:c226da522fbf7f9dbcfeeb7ed5ba578611febd5d660851faf8db4c2c0d29284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e34d5bfe7c3253fd115de860a3fc2451af1c5a25c32d19cf2562f50e91047a`

```dockerfile
```

-	Layers:
	-	`sha256:4d2e96d3c7680cd6abae8fbb5afde28134cb2b7594c42155cc33f5357db6e758`  
		Last Modified: Mon, 15 Jun 2026 18:38:09 GMT  
		Size: 8.2 MB (8182421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b778afffd5f4220306eee62b9d341a3c9c43b5b9780735591d0b617da2535366`  
		Last Modified: Mon, 15 Jun 2026 18:38:08 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9913645b0502208f2efdaa0c1bb34149fa59912b9f43556e6bf253e313bf227e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:72b64387a00eb1af2fde271b18ac92532ad8b810447fcde6c4858817b7b013dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325757133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1631f7fdcade9d29fa9ca86c566d7ad8ac97a548b86a57a25de9641b1cb826ef`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.version=20260614.0.544538
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.created=2026-06-14T00:09:34+00:00
# Mon, 15 Jun 2026 18:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Jun 2026 18:38:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260614.0.544538' /etc/os-release # buildkit
# Mon, 15 Jun 2026 18:38:55 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jun 2026 18:38:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5a7c0ae7636fdd5b0a3e918617dd5137091ba9d1fc005cea98693e7531a59bb2`  
		Last Modified: Mon, 15 Jun 2026 18:39:55 GMT  
		Size: 325.7 MB (325744576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf05f6fab31d37c6be2522ec8e5a555935626170962a5c71f2fcac0dea15bfdc`  
		Last Modified: Mon, 15 Jun 2026 18:39:46 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0971ed3c722d880bdd3b9bd8a78c27d2fa8b55b91d2fe8eca349a9c02eb51ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14668911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7c7f10c7feb73ecb20f27b3794b8e7af8ccc30c142b6f41828afe92afbd18b`

```dockerfile
```

-	Layers:
	-	`sha256:ab338090c90a4a7e8f53f5c9487c81cb29d21b311ad6613026f049ca5c70f90f`  
		Last Modified: Mon, 15 Jun 2026 18:39:47 GMT  
		Size: 14.7 MB (14657143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b42d7364101d932e2da886bc700b8db70f2af6ddd4d3d0a664c14478ac1f75`  
		Last Modified: Mon, 15 Jun 2026 18:39:46 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260621.0.546891`

**does not exist** (yet?)
