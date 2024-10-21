## `archlinux:base-devel-20241020.0.271562`

```console
$ docker pull archlinux@sha256:f493b023ea4e1dbc4073bf9f39898dfa153286f47547d1a5f886105e66557e5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241020.0.271562` - linux; amd64

```console
$ docker pull archlinux@sha256:bc750120ea9ea5b5f99248fe3cd9b22f85551883c0b1f4d3e59cd23c60791aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272210183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c7f3c47df3e45b4a24087b01b8b13cadfce0b5bf4870397dec0270c5c27cc4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20241020.0.271562
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-10-20T00:07:52+00:00
# Sun, 20 Oct 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241020.0.271562' /etc/os-release # buildkit
# Sun, 20 Oct 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 20 Oct 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:024e1215271164d7d8737dba631eaddb352b7bc965fb72669caed0e2e11e8691`  
		Last Modified: Mon, 21 Oct 2024 17:58:02 GMT  
		Size: 272.2 MB (272201158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4b88dd35c8937bcdda7d80a9ab0469d311f86f0910403ce62f7f0996cfa96d`  
		Last Modified: Mon, 21 Oct 2024 17:57:58 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241020.0.271562` - unknown; unknown

```console
$ docker pull archlinux@sha256:2099e7a9707bcdb7878c12b702c1ed3cff50026bc0aa5676ef4bd7d655370faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11957777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1584024742a905811323458f439fada2b4d0930b6c8f165f6b600be764e4ea84`

```dockerfile
```

-	Layers:
	-	`sha256:ba438d409d2d69beae59e756762cb69d164bd42ab3be2467b1c9542e8825fdef`  
		Last Modified: Mon, 21 Oct 2024 17:57:58 GMT  
		Size: 11.9 MB (11946240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18b546c38a04a8de21d0b9c536c80920f3a94e18db166f148fa91f3a7c84d10`  
		Last Modified: Mon, 21 Oct 2024 17:57:58 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
