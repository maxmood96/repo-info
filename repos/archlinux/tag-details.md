<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240804.0.251467`](#archlinuxbase-202408040251467)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240804.0.251467`](#archlinuxbase-devel-202408040251467)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240804.0.251467`](#archlinuxmultilib-devel-202408040251467)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:71b21b76a796b7d341b53be000b8e45dec6e5a800f209ec81e7518fbb3ae7e1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:486969816908ee2135d869bd7d3ca9bd15dc49f755e06f2d212915992b25b29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151248650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a865ea3c268ab91df55279608063e2f23ec9f95b05799afa47da0ff5c1a2f3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20240728.0.249973
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-07-28T00:07:38+00:00
# Sun, 28 Jul 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240728.0.249973' /etc/os-release # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 28 Jul 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2ddb01c0d7f6d92d20f27fd95db99c4c5a386cd8cfb1314b4a7b786572a7d794`  
		Last Modified: Mon, 29 Jul 2024 18:56:40 GMT  
		Size: 151.2 MB (151240373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c129c56407770f7db5dbbc74b5c35a38d7fe928643dd8f5656344d2ed2e1c14`  
		Last Modified: Mon, 29 Jul 2024 18:56:37 GMT  
		Size: 8.3 KB (8277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:9c1a0056bb068052d1200251d3f9936c761ce481b19fa98cfef16f04f9c45483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8117992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97233f85661203eca7fb0ef2547df5ba561410f7ebb86587b327e40c649c110`

```dockerfile
```

-	Layers:
	-	`sha256:7ed23936c13501de5387b6c2afec38634f3b9ebda476a094e4bf00a6f259789f`  
		Last Modified: Mon, 29 Jul 2024 18:56:37 GMT  
		Size: 8.1 MB (8106271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:febb2f070d08eb9aabbfaa9b9277e223f2d9d5036238cf45e963ff76d58f5043`  
		Last Modified: Mon, 29 Jul 2024 18:56:37 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240804.0.251467`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b110853598ac8526a6feb162b408d72fd45290efa6d8eba25753c9a49633709f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:519097be57855db5542c8f2ebd3adb3ecc227dcd5ac8a6a03abff54741fb177f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271740726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89f6c87211862b4036339df6f4049d107e8caa535fecc34e584ea010a076ac9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20240728.0.249973
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-07-28T00:07:38+00:00
# Sun, 28 Jul 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240728.0.249973' /etc/os-release # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 28 Jul 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:02456fbfa541313d4610d69c6ee80b0e3bd7e3af01f1215c5fd255c79c026988`  
		Last Modified: Mon, 29 Jul 2024 18:57:04 GMT  
		Size: 271.7 MB (271731685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1408e08202e0909786137de5d8856032d602ff18bdabb67b411c2ba43254e82`  
		Last Modified: Mon, 29 Jul 2024 18:57:01 GMT  
		Size: 9.0 KB (9041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:16da886ecc37a6f09f68e7db49a2ff483410edac825264f4e5d08f6b2be27132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11807894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0655e80220f6cc41f0f1f44cfa1b09b87d242675c33ea36d9536894d8660c0bd`

```dockerfile
```

-	Layers:
	-	`sha256:ee04007c105d1d87f18df366f2cf396daa7e38ac639a61db6d4d8073a83db654`  
		Last Modified: Mon, 29 Jul 2024 18:57:01 GMT  
		Size: 11.8 MB (11796391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8749cd4df133cb14387a58bdeda77ebedc394e4f41d6cf9618638585b42347f`  
		Last Modified: Mon, 29 Jul 2024 18:57:01 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240804.0.251467`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:71b21b76a796b7d341b53be000b8e45dec6e5a800f209ec81e7518fbb3ae7e1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:486969816908ee2135d869bd7d3ca9bd15dc49f755e06f2d212915992b25b29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151248650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a865ea3c268ab91df55279608063e2f23ec9f95b05799afa47da0ff5c1a2f3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20240728.0.249973
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-07-28T00:07:38+00:00
# Sun, 28 Jul 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240728.0.249973' /etc/os-release # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 28 Jul 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2ddb01c0d7f6d92d20f27fd95db99c4c5a386cd8cfb1314b4a7b786572a7d794`  
		Last Modified: Mon, 29 Jul 2024 18:56:40 GMT  
		Size: 151.2 MB (151240373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c129c56407770f7db5dbbc74b5c35a38d7fe928643dd8f5656344d2ed2e1c14`  
		Last Modified: Mon, 29 Jul 2024 18:56:37 GMT  
		Size: 8.3 KB (8277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:9c1a0056bb068052d1200251d3f9936c761ce481b19fa98cfef16f04f9c45483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8117992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97233f85661203eca7fb0ef2547df5ba561410f7ebb86587b327e40c649c110`

```dockerfile
```

-	Layers:
	-	`sha256:7ed23936c13501de5387b6c2afec38634f3b9ebda476a094e4bf00a6f259789f`  
		Last Modified: Mon, 29 Jul 2024 18:56:37 GMT  
		Size: 8.1 MB (8106271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:febb2f070d08eb9aabbfaa9b9277e223f2d9d5036238cf45e963ff76d58f5043`  
		Last Modified: Mon, 29 Jul 2024 18:56:37 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:485d4b471606e7e7e118b89f23ee59014338219861eb51e8682d9bc8c6212ad0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:78dac93b3899c3ca8da196f031c4269a2e922ff403cbb7033a77aa6d3b288bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321609342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c681f92f5bc3b27021717b33b0562ce6fab5ecbb9b2b28ebb7c0d5eee916b291`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20240728.0.249973
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-07-28T00:07:38+00:00
# Sun, 28 Jul 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240728.0.249973' /etc/os-release # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 28 Jul 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cfa234794e98e25410bbe10a20f100f1b0209775183d77be3028abd8feccc700`  
		Last Modified: Mon, 29 Jul 2024 18:57:16 GMT  
		Size: 321.6 MB (321599158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea515c7c1e758017809fc54cf4798e8eb2badf8a1a2744b10454735af3e29cf`  
		Last Modified: Mon, 29 Jul 2024 18:57:12 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f07c7ccd51b4553bd77877b81e46948143d6938d46b3822bc9b5adbb25c94ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0e88799e5886f93a81bc4716f727997ae0e4a6c3f482c4961b36bcfc921a89`

```dockerfile
```

-	Layers:
	-	`sha256:e8d9f04c64c88fa3ec9af0d39a76336bbccff9ed1a8bc51c8d7640161dd44934`  
		Last Modified: Mon, 29 Jul 2024 18:57:12 GMT  
		Size: 12.1 MB (12063678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50954966d24dc6f68cc45c527370572310767b83ae172eef67cae85348f9b54`  
		Last Modified: Mon, 29 Jul 2024 18:57:12 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240804.0.251467`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
