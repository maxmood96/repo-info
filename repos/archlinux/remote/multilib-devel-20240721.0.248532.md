## `archlinux:multilib-devel-20240721.0.248532`

```console
$ docker pull archlinux@sha256:1fdc4c5faac1b8cb347bd897103bd5431dae3e0e34067e131fc55f9761d6a45d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:8c4d9ef0c18a8dd6238d58736a14cdef7395509a9f1e3c4100942e43ba84bbc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321330216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4735d9134311d54edc7a0e33184c5b5a45c935109fcd3cf8def03b41a57e78`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:40dd90a9addf83cc89f51ca591fa1899c47712ae9d66995c5bcb684036b7f3b9`  
		Last Modified: Mon, 22 Jul 2024 19:59:36 GMT  
		Size: 321.3 MB (321320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8d694a178751287b41839cfc74ba49f9a9f8083b3ce036add39135c81ab851`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:617109e53823a36fb113b8227df712806fbd4bf88598e9919dca4ff906ff2c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12067542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aab41e7a2f1266889ab885a235fb175e4b01e177f50c8821c202d0603b97504`

```dockerfile
```

-	Layers:
	-	`sha256:2bc188ca5d15e72f2f7f20772645d4f0010204ab97b03111c4d50b64388df05b`  
		Last Modified: Mon, 22 Jul 2024 23:04:27 GMT  
		Size: 12.1 MB (12055983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8edbb02df9fca5b9c02ebe20fc29550e124a479ccbba3f183bee616acf2dcf23`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.in-toto+json
