## `archlinux:multilib-devel-20250608.0.361578`

```console
$ docker pull archlinux@sha256:37333001fa294ed7a7d24251bc2e9d4d1994179f41ab4824296917fb85655641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250608.0.361578` - linux; amd64

```console
$ docker pull archlinux@sha256:da861e322fb59830d475c836f19ddce01ed49b57d62da3412e2a20656d7fc666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338915575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d2e3c9ae7759a8e95c98da2d5344e656f5e879971d06bad78a13b397316dd2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.version=20250608.0.361578
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.created=2025-06-08T00:07:57+00:00
# Sun, 08 Jun 2025 00:07:57 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250608.0.361578' /etc/os-release # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
ENV LANG=C.UTF-8
# Sun, 08 Jun 2025 00:07:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ea7e7f76419f161d7e505b4739c95118b6711ff02193c3191043e82dfd0d77e0`  
		Last Modified: Mon, 09 Jun 2025 20:22:02 GMT  
		Size: 338.9 MB (338905315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e566327128d535b57df6147958cb3dcbcd2dec2bb700ee641e2e51480bc443`  
		Last Modified: Mon, 09 Jun 2025 19:10:31 GMT  
		Size: 10.3 KB (10260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250608.0.361578` - unknown; unknown

```console
$ docker pull archlinux@sha256:280f5d01ba094e5fb935ebd3f18b9b3ab68eb690e85d57d8c552a01e73ec36cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12287098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d7e266299c5d2e4628d8102c1064f632b5d7340d0624101b1929b9a84b70db`

```dockerfile
```

-	Layers:
	-	`sha256:3e53a7edde5327ab20078444499959f668c15587710b781d8183c90ee1533694`  
		Last Modified: Mon, 09 Jun 2025 22:48:27 GMT  
		Size: 12.3 MB (12275288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2308e8a46ecddf3a4044d82523454512cf8b9395f23ee4604d637fa51d3ab9`  
		Last Modified: Mon, 09 Jun 2025 22:48:27 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
