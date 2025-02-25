## `archlinux:latest`

```console
$ docker pull archlinux@sha256:0dd90d4fc8e6d991810f57222fa3a2d926b34e4aa3adb1117857c4685def16cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:a2ec6393d71cc4b5ec3b8749d6fb8ab46f3d7804542c778e58945425064a23a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158773606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0995e2d39d4e0e18432ae70b57f09667f40c6a73693dc9d294799696ab588e14`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:70c9c0bc740b2885ab94a3ed5f1f0f0d5c4e414d39b84d1a896a60ff68f74780`  
		Last Modified: Mon, 24 Feb 2025 20:29:08 GMT  
		Size: 158.8 MB (158765282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295b16ff000d323d54017b773a25cf28118f4ff9d132c428336b58a9babe9d`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d0fabb023c7544271b4bc385ab045839cdd95c469b6c8524c94c61df3875f1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8159967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651998445313026f641596942a94b3c3c28fe08a0f26b25cca5de3c7d39e0a07`

```dockerfile
```

-	Layers:
	-	`sha256:3f7f9721672652bba099e96c2ad82f525143eef1f3346b9592ebb454eea5cf05`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 8.1 MB (8147996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a40a8731b74907e6ec9938e258510eab4b3cf6fad27261516338d66a7d833b2`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json
