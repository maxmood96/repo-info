## `archlinux:multilib-devel-20240721.0.248532`

```console
$ docker pull archlinux@sha256:445ecfc82f497ec296ce3793b0310e0bc18013f3fd3ab8399033d5df595e1d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:2138a2444d1ce2c5b741e86cbafebc3f5635878d879a5f4dfd34fb737d0e80cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321330259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004c92c235e1b2ac1787a88c264b467db64725ed6a98027563363fba1b6533d1`
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
	-	`sha256:ead08b7f527112495853997c4f6e076297fafbeee4a4ff1bf40a2afd0ca6d008`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 10.2 KB (10227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:e6bd081033d4d5d84f94a11dfb2a126d62702446fd904c54d47d9ce354df56e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12067542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e9dac2e757edefc786d3b4e6108bcb7e76a331c4c9c710ff98fd42cc6d1f93`

```dockerfile
```

-	Layers:
	-	`sha256:99c4101fb50184fc9aae3e26d7520a4e08546cb5a44aa76aa19bb13fd24fe554`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 12.1 MB (12055983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec85316c8497a7c998b161253f89108c38e0fe32080efdafddf9f030e8b9a57f`  
		Last Modified: Mon, 22 Jul 2024 19:59:32 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.in-toto+json
