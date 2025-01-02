<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241229.0.293060`](#archlinuxbase-202412290293060)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241229.0.293060`](#archlinuxbase-devel-202412290293060)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241229.0.293060`](#archlinuxmultilib-devel-202412290293060)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:58fd363480dc61d0c657768605bca3c87d5b697cb8c2fe0217aad941c6a8a508
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:e6e48cdbca990bddabe31dccc340d3989cb6951380e3aa69b350e246a8f489c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152724049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d45be0b24be4f044711c0033fe7ee2265ea357134c82c2e4311ad1672eafb7c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241222.0.291122
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-12-22T00:07:56+00:00
# Sun, 22 Dec 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241222.0.291122' /etc/os-release # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 22 Dec 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7150b2dfc4ac7f06e85313fa003b954d50d19dcb209af67a1b1e297ea0ec9085`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 152.7 MB (152715741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6c0877756d57f5161544f13a5dd64e5653d5afa08880d6f8d0effaa659611`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 8.3 KB (8308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:284a09242e8ec48d05dbff4dfc1890d630d90749612b03079aecb3a09c64bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8087855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a089c590b6f05127ecff19707c673f5aa2e90fbae31d3c640e0ab99caf0baa8e`

```dockerfile
```

-	Layers:
	-	`sha256:af334dbbff0b5b9d2938efda66c9b20e1758b4f2cb1b121af3352ac80ac54c7e`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 8.1 MB (8075883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e111e40a728d2de21b287174abf303769fc7f548488d84eb6e1bc59c8cf4a63`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241229.0.293060`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:6112d42cc02db807bc8aeb512331d22be93f678ba68a4e4cafefa152da97c0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8d61f3ed74f269272e70df5e40195fc5308b400b9ed9da88c03d0e380604c612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273856065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2f651a08c1f04fe4eb40a719e7200a8848e5f13311b11ac914622dd1e3cf56`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241222.0.291122
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-12-22T00:07:56+00:00
# Sun, 22 Dec 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241222.0.291122' /etc/os-release # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 22 Dec 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7f4b5c3559686ed19ef1a63b1048727d14f71087a8f2e482d930dee90ac25b19`  
		Last Modified: Tue, 24 Dec 2024 21:33:14 GMT  
		Size: 273.8 MB (273846983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ea974a1247e9562262166cec5caa8e8f0cd897256fdccb8cdfd3c8008c4bba`  
		Last Modified: Tue, 24 Dec 2024 21:33:11 GMT  
		Size: 9.1 KB (9082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:7f516d7f3691dd40b709869b6ad47eae2925ac07bf07155d79fe7eff496a5c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11895046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324e5c9e86c044d42b86b4c483fdb67ae04ffd772269813058f11b8ce24a9f74`

```dockerfile
```

-	Layers:
	-	`sha256:001f3f15c7341e61ca0de99604726afc118d6de52fb9ed456c8672cf4548dc51`  
		Last Modified: Tue, 24 Dec 2024 21:33:11 GMT  
		Size: 11.9 MB (11883292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e644f21426b048723151e4d607b46caca834906cd0c7573d20fad233937f5a`  
		Last Modified: Tue, 24 Dec 2024 21:33:11 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241229.0.293060`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:58fd363480dc61d0c657768605bca3c87d5b697cb8c2fe0217aad941c6a8a508
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e6e48cdbca990bddabe31dccc340d3989cb6951380e3aa69b350e246a8f489c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152724049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d45be0b24be4f044711c0033fe7ee2265ea357134c82c2e4311ad1672eafb7c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241222.0.291122
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-12-22T00:07:56+00:00
# Sun, 22 Dec 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241222.0.291122' /etc/os-release # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 22 Dec 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7150b2dfc4ac7f06e85313fa003b954d50d19dcb209af67a1b1e297ea0ec9085`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 152.7 MB (152715741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6c0877756d57f5161544f13a5dd64e5653d5afa08880d6f8d0effaa659611`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 8.3 KB (8308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:284a09242e8ec48d05dbff4dfc1890d630d90749612b03079aecb3a09c64bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8087855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a089c590b6f05127ecff19707c673f5aa2e90fbae31d3c640e0ab99caf0baa8e`

```dockerfile
```

-	Layers:
	-	`sha256:af334dbbff0b5b9d2938efda66c9b20e1758b4f2cb1b121af3352ac80ac54c7e`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 8.1 MB (8075883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e111e40a728d2de21b287174abf303769fc7f548488d84eb6e1bc59c8cf4a63`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:67704f0a23cb6c4f127cc0f273f9980ed295f7eb9ce427e6f4177c1a0f4d08bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:06b88c7713d80627f71d38f3bc4098759e1f11efb3497f1a4b293d276d53651e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323697247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0847da9bca4d728a7ae8b61e844fa1da1971717e14d97beab7d4817b300361`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241222.0.291122
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-12-22T00:07:56+00:00
# Sun, 22 Dec 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241222.0.291122' /etc/os-release # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 22 Dec 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4bbe098a76a09b2e2fddeefd75ddf1e3f6efff78d5b7e29f298df0963e2d73a0`  
		Last Modified: Tue, 24 Dec 2024 21:33:42 GMT  
		Size: 323.7 MB (323687046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486374b3ba3fde819abf241b81da0fc83841d5d1200b2a96e256cbe76fb57a04`  
		Last Modified: Tue, 24 Dec 2024 21:33:35 GMT  
		Size: 10.2 KB (10201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:022e1290962ff7e859ae28f621c044d87973357c6a58ff2ddabfa5a984404cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12163576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac4cde9a8fedfd5564b62cff4c324f9e8e14e080c9ffab534a426c613ab398`

```dockerfile
```

-	Layers:
	-	`sha256:1e933bbcc018b86add4a62ce900a0322c353dd7f9d4382cc4514ccf5329078d8`  
		Last Modified: Tue, 24 Dec 2024 21:33:36 GMT  
		Size: 12.2 MB (12151765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d0adb43149d3b3467b83b59975adae53ba0852d1e37ec3e09daf3a31b124f9a`  
		Last Modified: Tue, 24 Dec 2024 21:33:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241229.0.293060`

**does not exist** (yet?)
