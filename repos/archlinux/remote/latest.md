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
