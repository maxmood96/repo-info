## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:16a5c1e25bbfe5de4d04944f5a6ebdf49e8517a14451cb9587f5185129467161
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6bb5912933272ebe9eb8e21a1b97993b1ab8e1ddaf274ae8f2280194afe479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321524297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1161492424c04ae736a6eb14251b8e79163426b0213ec0d36a4fc58d172c66d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.version=20240804.0.251467
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.created=2024-08-04T00:07:42+00:00
# Sun, 04 Aug 2024 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240804.0.251467' /etc/os-release # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 04 Aug 2024 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e84faef981553e49ef881afdcdc205918123010107a998eadc5fa3573a44ea81`  
		Last Modified: Mon, 05 Aug 2024 18:58:22 GMT  
		Size: 321.5 MB (321514113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c192d2661aebb550035aeda900a25ed59b022c0b42a6034031463bc6d15922`  
		Last Modified: Mon, 05 Aug 2024 18:58:17 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3c4820c32b6883e48ca2918725e3fac98d78fdd108f50f9a0df4a3091375479c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12072744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d23d9f92f8ddf22cb27652f9ad105de9bd761430fd75e65ebf4808b1b92b32e`

```dockerfile
```

-	Layers:
	-	`sha256:9a9d97c4003f6d5f3e2f4a28c5e4a3bd4cb74ad2ff52ace3fe11446af6fa7df0`  
		Last Modified: Mon, 05 Aug 2024 18:58:17 GMT  
		Size: 12.1 MB (12061186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2de089a1b11192ab1bee8c4ab60f7aa1e0b020b4f6557f630fe3e7102cdd098`  
		Last Modified: Mon, 05 Aug 2024 18:58:17 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json
