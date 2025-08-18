## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:10f14c98fb1a3476d89db888e853eb5259adec84caa5eb485316a318ba534833
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:17f7931d409b49b29da5486ba061cae7b88b2fb3703591c69fe39d437123a35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340447562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584e670b4e0b5660d130d2d52b65105d3a7f7c2b096ad8b0754db3e4b1a9f2a9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.version=20250817.0.405639
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.created=2025-08-17T00:07:25+00:00
# Sun, 17 Aug 2025 00:07:25 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250817.0.405639' /etc/os-release # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
ENV LANG=C.UTF-8
# Sun, 17 Aug 2025 00:07:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1f2b41bf42c3a563055da325cf677ade819fecdde00b8981ef0f240a7a68daf4`  
		Last Modified: Mon, 18 Aug 2025 17:09:13 GMT  
		Size: 340.4 MB (340437287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195cfba426c73771598e59b62a71a5d342cdc662606b8444df994f12b22d7e01`  
		Last Modified: Mon, 18 Aug 2025 16:55:09 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:70a921b5e4fa55e79d8c7518aaa8bce88869376e51298e43e3f4a587c704c3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12344512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8368a2b68ba64bf308c897baf8fbb432f26706d862cde29164fd8b137acb5393`

```dockerfile
```

-	Layers:
	-	`sha256:9d95aa728609f34ed9d726672de45c161d1f380a9b22e5b9bc424c1eb2b45b74`  
		Last Modified: Mon, 18 Aug 2025 19:48:27 GMT  
		Size: 12.3 MB (12332701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d95c675b5cfe267be978d766b6900a7100c4289c361ee188bc44266a7216981`  
		Last Modified: Mon, 18 Aug 2025 19:48:27 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
