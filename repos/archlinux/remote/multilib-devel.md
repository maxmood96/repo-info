## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:2a6d6172047c9b6c27f772a91500717c0eddff4cceabe8f0791c4387745efb93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7a87aef720d50d76e8d40edb4d1cc65f3ddeca86d0aaabd877b8390e751f33a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322058840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b097299855429aa5de6b4381218c344872399c99e54cf495e32f89b3dbc954e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Oct 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
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
	-	`sha256:fddc4115830b94cf3617c5c01934353eff594fc95ce15d3ab01cf59987bbaeaa`  
		Last Modified: Mon, 21 Oct 2024 17:58:09 GMT  
		Size: 322.0 MB (322048722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca489cfbc6b5c3f92d35d06d6c9dda00cb6e5283e4a23767e4ed388f980345b4`  
		Last Modified: Mon, 21 Oct 2024 17:58:05 GMT  
		Size: 10.1 KB (10118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:7a26696b80cbb6f623b8eb0ea368556c353d2fa70ff8041e13c03584a0d9a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12226630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6150a8e7914c52f2df86036903fb680c84c4cbee55df4a5d3b8a1481796df5`

```dockerfile
```

-	Layers:
	-	`sha256:58399ad9e575fb269b2d56c39f95f8765be1123fb83551015fda7bcaf24a09f7`  
		Last Modified: Mon, 21 Oct 2024 17:58:05 GMT  
		Size: 12.2 MB (12215036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15139c3ed67f1cec28146bd2425a4cde791a88b11f432cac6d34b60fab53fd4a`  
		Last Modified: Mon, 21 Oct 2024 17:58:05 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json
