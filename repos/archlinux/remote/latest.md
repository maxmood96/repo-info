## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a750678fba4213b3d4054b88218b314733594e887d44be2a59fdf61cf6a5c641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:649f22ffe44950a2fbdd7b4f3ad7eaf1ae017d60360f857ba1b07902121824d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151193892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd09adc826967eb17f91d1b34e2f25a5bacb786a7d2daa7b42ab8726ce296cd`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.version=20240818.0.255804
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.created=2024-08-18T00:07:58+00:00
# Sun, 18 Aug 2024 00:07:58 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240818.0.255804' /etc/os-release # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 18 Aug 2024 00:07:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9ed62a58ff74bd4fb28a245ec0e2ccba3ffe5d464456f8e0deedb4e20501291a`  
		Last Modified: Mon, 19 Aug 2024 17:57:40 GMT  
		Size: 151.2 MB (151185620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00da84d1f8972f5df6c181e1d3fbff6c3f801c27dee24820bec518e802577bc`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 8.3 KB (8272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d97ca1db468c618434ab7ffe94bbcad8c8a42ac29719b47916d634c9e47ff671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c29c967e415355d4f29d75cc6a91fba3ec01900d2ea620f97c0a895dd364942`

```dockerfile
```

-	Layers:
	-	`sha256:f8a51f688d53dc94414d7de4e91bddd8f54788b4c2aa2fe570b72fe692b759fb`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 8.1 MB (8103931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f853272c82e70efd1417a28fba73b4ed94db1220a8a0e0395802fbb38ecdd3`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json
