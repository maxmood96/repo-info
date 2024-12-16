<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241215.0.289170`](#archlinuxbase-202412150289170)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241215.0.289170`](#archlinuxbase-devel-202412150289170)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241215.0.289170`](#archlinuxmultilib-devel-202412150289170)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:901cf83a14f09d9ba70b219e22f67abd4d6346cb6d3f0c048cd08f22fb9a7425
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c6adc95d0eabb024edace76211d96a1c43846e475eee5ce7bbf71a444d332bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152724438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4c632eebd620b4f6201d93de0f3f339423c283c08aa3d7fc706c2797150e45`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7fa4bb7a964dac0c4b221a145e2f663e66dbe8ad7db623df9a05ea30a7c21cc3`  
		Last Modified: Mon, 16 Dec 2024 18:28:34 GMT  
		Size: 152.7 MB (152716125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d609407a8e75eb4be7200f664d3e143be31dc28d208ba378633e1bb3605ad0`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 8.3 KB (8313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:944eabb17f6b795d6dcd8f157b3bfc383572f18aaa45b1462d1b0e342f357e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32a9b110dfd18d83ca8c8036b661cb40e1d5587fd59a1d2ae463987b87501`

```dockerfile
```

-	Layers:
	-	`sha256:aaec2d5338db11b50ca421b7cf99f0003a95b5308230b51736e08bf39306025c`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 8.1 MB (8089382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38229154eaac88caa23c818b99f6721a148abe74011f18b22a1ac82c866c0b01`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241215.0.289170`

```console
$ docker pull archlinux@sha256:901cf83a14f09d9ba70b219e22f67abd4d6346cb6d3f0c048cd08f22fb9a7425
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20241215.0.289170` - linux; amd64

```console
$ docker pull archlinux@sha256:c6adc95d0eabb024edace76211d96a1c43846e475eee5ce7bbf71a444d332bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152724438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4c632eebd620b4f6201d93de0f3f339423c283c08aa3d7fc706c2797150e45`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7fa4bb7a964dac0c4b221a145e2f663e66dbe8ad7db623df9a05ea30a7c21cc3`  
		Last Modified: Mon, 16 Dec 2024 18:28:34 GMT  
		Size: 152.7 MB (152716125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d609407a8e75eb4be7200f664d3e143be31dc28d208ba378633e1bb3605ad0`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 8.3 KB (8313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20241215.0.289170` - unknown; unknown

```console
$ docker pull archlinux@sha256:944eabb17f6b795d6dcd8f157b3bfc383572f18aaa45b1462d1b0e342f357e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32a9b110dfd18d83ca8c8036b661cb40e1d5587fd59a1d2ae463987b87501`

```dockerfile
```

-	Layers:
	-	`sha256:aaec2d5338db11b50ca421b7cf99f0003a95b5308230b51736e08bf39306025c`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 8.1 MB (8089382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38229154eaac88caa23c818b99f6721a148abe74011f18b22a1ac82c866c0b01`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:cc49f48d188c483c30ea97ea9d72a60320268ba41dc390a84b49931ede212323
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:184dc07718fbfbd7e91b4451f319e15b3051a760de461a7f0cc2506d0f2355e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273856234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa56e074c40961284b699a46d0ca465f847bdebbe8e2a3a144d58b8482ed1c72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a629b563c7867e18ee942f491f3b1671d6bbbc3b986cf5208a6776d910507c5`  
		Last Modified: Mon, 16 Dec 2024 18:29:05 GMT  
		Size: 273.8 MB (273847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d360bd31154f915de54aadd523646c3c3e6d270b8fbf97c74308104dace7fe`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 9.1 KB (9108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0ddbc0c3c10c63175620fb884e53936b7fa47bcc83f479e6972b0d54079329b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11914779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe6da1cc9135248b585cc99893a06ff7263a3c21d04410f3559455a3dff4993`

```dockerfile
```

-	Layers:
	-	`sha256:7aedc5df46a740cb695f491deceb7c0fa0e88ae6a8a1b47f81237aa90163e2be`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 11.9 MB (11903025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07602835f1f406328928e1f9024ede80ce4dabf10fb3a57b193c6f6604afb392`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241215.0.289170`

```console
$ docker pull archlinux@sha256:cc49f48d188c483c30ea97ea9d72a60320268ba41dc390a84b49931ede212323
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241215.0.289170` - linux; amd64

```console
$ docker pull archlinux@sha256:184dc07718fbfbd7e91b4451f319e15b3051a760de461a7f0cc2506d0f2355e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273856234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa56e074c40961284b699a46d0ca465f847bdebbe8e2a3a144d58b8482ed1c72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a629b563c7867e18ee942f491f3b1671d6bbbc3b986cf5208a6776d910507c5`  
		Last Modified: Mon, 16 Dec 2024 18:29:05 GMT  
		Size: 273.8 MB (273847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d360bd31154f915de54aadd523646c3c3e6d270b8fbf97c74308104dace7fe`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 9.1 KB (9108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241215.0.289170` - unknown; unknown

```console
$ docker pull archlinux@sha256:0ddbc0c3c10c63175620fb884e53936b7fa47bcc83f479e6972b0d54079329b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11914779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe6da1cc9135248b585cc99893a06ff7263a3c21d04410f3559455a3dff4993`

```dockerfile
```

-	Layers:
	-	`sha256:7aedc5df46a740cb695f491deceb7c0fa0e88ae6a8a1b47f81237aa90163e2be`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 11.9 MB (11903025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07602835f1f406328928e1f9024ede80ce4dabf10fb3a57b193c6f6604afb392`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:901cf83a14f09d9ba70b219e22f67abd4d6346cb6d3f0c048cd08f22fb9a7425
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c6adc95d0eabb024edace76211d96a1c43846e475eee5ce7bbf71a444d332bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152724438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4c632eebd620b4f6201d93de0f3f339423c283c08aa3d7fc706c2797150e45`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7fa4bb7a964dac0c4b221a145e2f663e66dbe8ad7db623df9a05ea30a7c21cc3`  
		Last Modified: Mon, 16 Dec 2024 18:28:34 GMT  
		Size: 152.7 MB (152716125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d609407a8e75eb4be7200f664d3e143be31dc28d208ba378633e1bb3605ad0`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 8.3 KB (8313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:944eabb17f6b795d6dcd8f157b3bfc383572f18aaa45b1462d1b0e342f357e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32a9b110dfd18d83ca8c8036b661cb40e1d5587fd59a1d2ae463987b87501`

```dockerfile
```

-	Layers:
	-	`sha256:aaec2d5338db11b50ca421b7cf99f0003a95b5308230b51736e08bf39306025c`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 8.1 MB (8089382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38229154eaac88caa23c818b99f6721a148abe74011f18b22a1ac82c866c0b01`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:973e63a746e98bc3dddf3413cd7cee3f6b9fc8de82514b6148247e2377fd8e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5b0411eb075d715a50043661da62120614db5bfeeede079d14be45a98c3c3988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323695018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1db025db8e7ea6ea6026f5abf0bc67b2b86a3db26907f2e7a4193f849365ad3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8c71d34480bb730e614fccaf4fdaec4f8fb129bdc3b8894eeedbb5c560a24b9f`  
		Last Modified: Mon, 16 Dec 2024 18:29:42 GMT  
		Size: 323.7 MB (323684798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c9ba2ebeeafc2947b037a964cae144a0560b9ba5bf49df78519b9e9df5ee6`  
		Last Modified: Mon, 16 Dec 2024 18:29:35 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:9b0b66148c3b46fd3ef4defea8305e5e5614ceabd5bcd0a8c59d4a1428da343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12183700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf91482063b88dc991538a26f55253c47974bc0f31dc62473154ce9b6b8cea43`

```dockerfile
```

-	Layers:
	-	`sha256:1fa6c3dfe13b4f13991a156daa36781b8ca6336bf6421d0447e6925e039c885f`  
		Last Modified: Mon, 16 Dec 2024 18:29:36 GMT  
		Size: 12.2 MB (12171890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8257273bb029eed1577b8891c02891d90c29d7d69cd9ce7f14cc86c2ec2511c7`  
		Last Modified: Mon, 16 Dec 2024 18:29:35 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241215.0.289170`

```console
$ docker pull archlinux@sha256:973e63a746e98bc3dddf3413cd7cee3f6b9fc8de82514b6148247e2377fd8e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241215.0.289170` - linux; amd64

```console
$ docker pull archlinux@sha256:5b0411eb075d715a50043661da62120614db5bfeeede079d14be45a98c3c3988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323695018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1db025db8e7ea6ea6026f5abf0bc67b2b86a3db26907f2e7a4193f849365ad3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8c71d34480bb730e614fccaf4fdaec4f8fb129bdc3b8894eeedbb5c560a24b9f`  
		Last Modified: Mon, 16 Dec 2024 18:29:42 GMT  
		Size: 323.7 MB (323684798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c9ba2ebeeafc2947b037a964cae144a0560b9ba5bf49df78519b9e9df5ee6`  
		Last Modified: Mon, 16 Dec 2024 18:29:35 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241215.0.289170` - unknown; unknown

```console
$ docker pull archlinux@sha256:9b0b66148c3b46fd3ef4defea8305e5e5614ceabd5bcd0a8c59d4a1428da343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12183700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf91482063b88dc991538a26f55253c47974bc0f31dc62473154ce9b6b8cea43`

```dockerfile
```

-	Layers:
	-	`sha256:1fa6c3dfe13b4f13991a156daa36781b8ca6336bf6421d0447e6925e039c885f`  
		Last Modified: Mon, 16 Dec 2024 18:29:36 GMT  
		Size: 12.2 MB (12171890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8257273bb029eed1577b8891c02891d90c29d7d69cd9ce7f14cc86c2ec2511c7`  
		Last Modified: Mon, 16 Dec 2024 18:29:35 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
