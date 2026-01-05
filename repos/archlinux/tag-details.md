<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260104.0.477168`](#archlinuxbase-202601040477168)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260104.0.477168`](#archlinuxbase-devel-202601040477168)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260104.0.477168`](#archlinuxmultilib-devel-202601040477168)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:601140151f85e9f33ac42ebdd671061b109ad3ed83d794e2399bbfa6ccf30543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9196779c67e7509190eccbfd1a5149cbf43712bfd142dba8d893fe291912b852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174698916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddb1ff8c1c65c7a3bc3d3b2bf28d1ac30edc9ab525c1cdfaaa652c462db7c1e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:16:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:16:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:16:16 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:16:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:74d5579544e6f07f058114dd075f29694904ace100d660e3a2db3086d13ef796`  
		Last Modified: Mon, 05 Jan 2026 18:17:36 GMT  
		Size: 174.7 MB (174690249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920abf4e07e67ddc3105f7a0e85308fbcdb232b073d817adc40f1f048c92dd`  
		Last Modified: Mon, 05 Jan 2026 18:17:06 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:9f7a0c109b5d4f6965b049b94057e6ba33b69df49f0f3e8aad409745ed453e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755165ae56408573555e536074dbc169adfcd95711f4377dc369c4bf42cdbbec`

```dockerfile
```

-	Layers:
	-	`sha256:3c234121efd0eda9b56a029e610b3af82f4a0d24da77b5de71d10cd67e856718`  
		Last Modified: Mon, 05 Jan 2026 20:48:16 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfba4161778a662772d8088f287c9b9469556bf6b6850661db05606515d3865c`  
		Last Modified: Mon, 05 Jan 2026 20:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260104.0.477168`

```console
$ docker pull archlinux@sha256:601140151f85e9f33ac42ebdd671061b109ad3ed83d794e2399bbfa6ccf30543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260104.0.477168` - linux; amd64

```console
$ docker pull archlinux@sha256:9196779c67e7509190eccbfd1a5149cbf43712bfd142dba8d893fe291912b852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174698916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddb1ff8c1c65c7a3bc3d3b2bf28d1ac30edc9ab525c1cdfaaa652c462db7c1e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:16:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:16:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:16:16 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:16:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:74d5579544e6f07f058114dd075f29694904ace100d660e3a2db3086d13ef796`  
		Last Modified: Mon, 05 Jan 2026 18:17:36 GMT  
		Size: 174.7 MB (174690249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920abf4e07e67ddc3105f7a0e85308fbcdb232b073d817adc40f1f048c92dd`  
		Last Modified: Mon, 05 Jan 2026 18:17:06 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260104.0.477168` - unknown; unknown

```console
$ docker pull archlinux@sha256:9f7a0c109b5d4f6965b049b94057e6ba33b69df49f0f3e8aad409745ed453e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755165ae56408573555e536074dbc169adfcd95711f4377dc369c4bf42cdbbec`

```dockerfile
```

-	Layers:
	-	`sha256:3c234121efd0eda9b56a029e610b3af82f4a0d24da77b5de71d10cd67e856718`  
		Last Modified: Mon, 05 Jan 2026 20:48:16 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfba4161778a662772d8088f287c9b9469556bf6b6850661db05606515d3865c`  
		Last Modified: Mon, 05 Jan 2026 20:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:ebcaeca69c4d416f848aedcd27fe224384fd506f86046526a5d49ec6d9e29db1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ead95833f3f1ed3c9091b46ad6cb5fb2d74059563ae2103a571dfb7b9dc3dac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292240275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08743ab9e023f5fb8785572404c676b3b08ba5688ffe56d3a8fdf33cd5fcf025`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:17:31 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:17:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:17:38 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:17:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:eb6edcde3302363203e3f39893a530aa11ed565f5ed4627a0d7e1f2000bf8ec5`  
		Last Modified: Mon, 05 Jan 2026 18:18:56 GMT  
		Size: 292.2 MB (292231101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0aac60a122f2991c855cdcd7e0d24ac09592fb1d27e166496c75bb58963e5`  
		Last Modified: Mon, 05 Jan 2026 18:18:46 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:b0fc54738d748505da84b1863693a0936ce40b53bab34e9f4ab584e2bda9110d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12157441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f95b3a321ddb4960b838cc642749398c97374a3d72aa8b71e2a6a3d16c36bd`

```dockerfile
```

-	Layers:
	-	`sha256:e46139c11b088c470d1b181ce963da28489c53bd9ed6574f73a09f6f99aabb19`  
		Last Modified: Mon, 05 Jan 2026 20:48:24 GMT  
		Size: 12.1 MB (12145730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ba6472061812c247ad8f6be05c64ab2fbd67e4a0a6290a411940dff9c7306b`  
		Last Modified: Mon, 05 Jan 2026 20:48:25 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260104.0.477168`

```console
$ docker pull archlinux@sha256:ebcaeca69c4d416f848aedcd27fe224384fd506f86046526a5d49ec6d9e29db1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260104.0.477168` - linux; amd64

```console
$ docker pull archlinux@sha256:ead95833f3f1ed3c9091b46ad6cb5fb2d74059563ae2103a571dfb7b9dc3dac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292240275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08743ab9e023f5fb8785572404c676b3b08ba5688ffe56d3a8fdf33cd5fcf025`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:17:31 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:17:31 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:17:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:17:38 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:17:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:eb6edcde3302363203e3f39893a530aa11ed565f5ed4627a0d7e1f2000bf8ec5`  
		Last Modified: Mon, 05 Jan 2026 18:18:56 GMT  
		Size: 292.2 MB (292231101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0aac60a122f2991c855cdcd7e0d24ac09592fb1d27e166496c75bb58963e5`  
		Last Modified: Mon, 05 Jan 2026 18:18:46 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260104.0.477168` - unknown; unknown

```console
$ docker pull archlinux@sha256:b0fc54738d748505da84b1863693a0936ce40b53bab34e9f4ab584e2bda9110d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12157441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f95b3a321ddb4960b838cc642749398c97374a3d72aa8b71e2a6a3d16c36bd`

```dockerfile
```

-	Layers:
	-	`sha256:e46139c11b088c470d1b181ce963da28489c53bd9ed6574f73a09f6f99aabb19`  
		Last Modified: Mon, 05 Jan 2026 20:48:24 GMT  
		Size: 12.1 MB (12145730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ba6472061812c247ad8f6be05c64ab2fbd67e4a0a6290a411940dff9c7306b`  
		Last Modified: Mon, 05 Jan 2026 20:48:25 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:601140151f85e9f33ac42ebdd671061b109ad3ed83d794e2399bbfa6ccf30543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9196779c67e7509190eccbfd1a5149cbf43712bfd142dba8d893fe291912b852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174698916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddb1ff8c1c65c7a3bc3d3b2bf28d1ac30edc9ab525c1cdfaaa652c462db7c1e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:16:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:16:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:16:16 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:16:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:74d5579544e6f07f058114dd075f29694904ace100d660e3a2db3086d13ef796`  
		Last Modified: Mon, 05 Jan 2026 18:17:36 GMT  
		Size: 174.7 MB (174690249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920abf4e07e67ddc3105f7a0e85308fbcdb232b073d817adc40f1f048c92dd`  
		Last Modified: Mon, 05 Jan 2026 18:17:06 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:9f7a0c109b5d4f6965b049b94057e6ba33b69df49f0f3e8aad409745ed453e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755165ae56408573555e536074dbc169adfcd95711f4377dc369c4bf42cdbbec`

```dockerfile
```

-	Layers:
	-	`sha256:3c234121efd0eda9b56a029e610b3af82f4a0d24da77b5de71d10cd67e856718`  
		Last Modified: Mon, 05 Jan 2026 20:48:16 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfba4161778a662772d8088f287c9b9469556bf6b6850661db05606515d3865c`  
		Last Modified: Mon, 05 Jan 2026 20:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:400068c34425fddb5c5e1120e55f0cc30603d798cdef20d782d75768ff42aa22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ad458d551f760c99654cbadaf418f9d52511604462be3838fe183a6d042b58a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343555316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58c3573b89670d991522dc02fe0af37058eb86726274fbc857faaf48d697f11`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:18:08 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:18:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:18:16 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:18:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4d8551d0b9caf25071addc6296ecff628973b4a1a667a059e49416651d1c7c69`  
		Last Modified: Mon, 05 Jan 2026 18:19:57 GMT  
		Size: 343.5 MB (343545027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf22f956b7a5c45d9c5f5f4173de6f3a94afae9cd604a8becb0ff08f8fa44ec`  
		Last Modified: Mon, 05 Jan 2026 18:19:22 GMT  
		Size: 10.3 KB (10289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:688beac2cd317902b7090fe5cb9ed03a86c232ca342c0a228ecd9065e50d7a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac60ffb3e72456f93090eff387acd287765fe0df936a0ca9bf2f8d80d002095`

```dockerfile
```

-	Layers:
	-	`sha256:4e57fa88627ab907121956a8754186cc6e5d9d7a73927afb2fe4436e042e5033`  
		Last Modified: Mon, 05 Jan 2026 20:48:32 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b40d404f0849662b16f2ef8020130fb4e98daf60a5a01dbcc380c18a7412bc5`  
		Last Modified: Mon, 05 Jan 2026 20:48:33 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260104.0.477168`

```console
$ docker pull archlinux@sha256:400068c34425fddb5c5e1120e55f0cc30603d798cdef20d782d75768ff42aa22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260104.0.477168` - linux; amd64

```console
$ docker pull archlinux@sha256:ad458d551f760c99654cbadaf418f9d52511604462be3838fe183a6d042b58a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343555316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58c3573b89670d991522dc02fe0af37058eb86726274fbc857faaf48d697f11`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:18:08 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:18:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:18:16 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:18:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4d8551d0b9caf25071addc6296ecff628973b4a1a667a059e49416651d1c7c69`  
		Last Modified: Mon, 05 Jan 2026 18:19:57 GMT  
		Size: 343.5 MB (343545027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf22f956b7a5c45d9c5f5f4173de6f3a94afae9cd604a8becb0ff08f8fa44ec`  
		Last Modified: Mon, 05 Jan 2026 18:19:22 GMT  
		Size: 10.3 KB (10289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260104.0.477168` - unknown; unknown

```console
$ docker pull archlinux@sha256:688beac2cd317902b7090fe5cb9ed03a86c232ca342c0a228ecd9065e50d7a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac60ffb3e72456f93090eff387acd287765fe0df936a0ca9bf2f8d80d002095`

```dockerfile
```

-	Layers:
	-	`sha256:4e57fa88627ab907121956a8754186cc6e5d9d7a73927afb2fe4436e042e5033`  
		Last Modified: Mon, 05 Jan 2026 20:48:32 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b40d404f0849662b16f2ef8020130fb4e98daf60a5a01dbcc380c18a7412bc5`  
		Last Modified: Mon, 05 Jan 2026 20:48:33 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
