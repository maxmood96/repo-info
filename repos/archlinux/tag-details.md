<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20230625.0.160368`](#archlinuxbase-202306250160368)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20230625.0.160368`](#archlinuxbase-devel-202306250160368)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:28cafcbd4df875971df45047bbbe80882e0cd7a8bfa02ff6bb4f702e0a3f87a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:707c4cb0473b45bdeb3664a85d1c8888f7d9143ced98d895eba138126d68e506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146081467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42ba935fd733f8e8c115266ba8b15a17a2582675f1adfa4de76f1c4e7dcf4fa`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jun 2023 18:19:58 GMT
LABEL org.opencontainers.image.version=20230611.0.157136
# Mon, 12 Jun 2023 18:19:58 GMT
LABEL org.opencontainers.image.revision=a395f71b6337b7612e5749a62698d598869059f0
# Mon, 12 Jun 2023 18:19:58 GMT
LABEL org.opencontainers.image.created=2023-06-11T00:06:39+00:00
# Mon, 12 Jun 2023 18:20:04 GMT
COPY dir:5bcbc6d753462b5256bd3e682323362d50da99be384069b33450827f76bbb1bb in / 
# Mon, 12 Jun 2023 18:20:05 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230611.0.157136' /etc/os-release
# Mon, 12 Jun 2023 18:20:06 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 18:20:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:24b6781efae184a0dd5da2812c18520bddb8538ea18f932871421d68416ec6b9`  
		Last Modified: Mon, 12 Jun 2023 18:21:46 GMT  
		Size: 146.1 MB (146073429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36877412a69b61b281f8ded424fd81ffec69849b8d0094e98cf73ad068a7754d`  
		Last Modified: Mon, 12 Jun 2023 18:21:27 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20230625.0.160368`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c1cc82cde7e0439dc17ade3633bc8daf92a8ce11990311d02b17ec14e3db959d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0b5b4c527e4178d8a53cf16f6fb7638113bd9d0e0957f49062e0efa8933fc464
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253102605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ce5c195686460e4328f132ad17306d0f6f921b45d6c741a7ace4acc5096d54`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.version=20230611.0.157136
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.revision=a395f71b6337b7612e5749a62698d598869059f0
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.created=2023-06-11T00:06:42+00:00
# Mon, 12 Jun 2023 18:21:06 GMT
COPY dir:7e9aa3d0c345b7975af4ef389e1b18fe37ab765e6100f5c664aa23848e051f28 in / 
# Mon, 12 Jun 2023 18:21:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230611.0.157136' /etc/os-release
# Mon, 12 Jun 2023 18:21:09 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 18:21:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6492817d4306b8b0b97c1c8166313cd21155b4a05fb4c6af7f03acf4bd55b631`  
		Last Modified: Mon, 12 Jun 2023 18:22:32 GMT  
		Size: 253.1 MB (253093881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5486ada8851810b1e00ad1bf79f94e7a2cbbd649e3cb220b56dc21b506bc9886`  
		Last Modified: Mon, 12 Jun 2023 18:21:58 GMT  
		Size: 8.7 KB (8724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20230625.0.160368`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:28cafcbd4df875971df45047bbbe80882e0cd7a8bfa02ff6bb4f702e0a3f87a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:707c4cb0473b45bdeb3664a85d1c8888f7d9143ced98d895eba138126d68e506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146081467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42ba935fd733f8e8c115266ba8b15a17a2582675f1adfa4de76f1c4e7dcf4fa`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jun 2023 18:19:58 GMT
LABEL org.opencontainers.image.version=20230611.0.157136
# Mon, 12 Jun 2023 18:19:58 GMT
LABEL org.opencontainers.image.revision=a395f71b6337b7612e5749a62698d598869059f0
# Mon, 12 Jun 2023 18:19:58 GMT
LABEL org.opencontainers.image.created=2023-06-11T00:06:39+00:00
# Mon, 12 Jun 2023 18:20:04 GMT
COPY dir:5bcbc6d753462b5256bd3e682323362d50da99be384069b33450827f76bbb1bb in / 
# Mon, 12 Jun 2023 18:20:05 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230611.0.157136' /etc/os-release
# Mon, 12 Jun 2023 18:20:06 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 18:20:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:24b6781efae184a0dd5da2812c18520bddb8538ea18f932871421d68416ec6b9`  
		Last Modified: Mon, 12 Jun 2023 18:21:46 GMT  
		Size: 146.1 MB (146073429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36877412a69b61b281f8ded424fd81ffec69849b8d0094e98cf73ad068a7754d`  
		Last Modified: Mon, 12 Jun 2023 18:21:27 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
