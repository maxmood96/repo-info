## `archlinux:base-devel-20250420.0.338771`

```console
$ docker pull archlinux@sha256:ef9c9e84828ccedb4cbabfe0a23f636ccd01151c89cad04401afdae4454c2312
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250420.0.338771` - linux; amd64

```console
$ docker pull archlinux@sha256:54c1922f68a1de47fed8b7d6d1db54f555bbd40cbe8e01aa593a2b81be1add6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281760687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781c7b01102859435fa5c5455647eb06070fa91767bbafe89ae28637356aae4e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:83f4100c1b5735024afce8e791c4d3749fe3f86b087ab0210426a12332693945`  
		Last Modified: Mon, 21 Apr 2025 22:34:49 GMT  
		Size: 281.8 MB (281751516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa612d5cc862eac9104b82df9bcbbc7d20689d0086fff0ed0acdddf83b038c4`  
		Last Modified: Mon, 21 Apr 2025 22:34:45 GMT  
		Size: 9.2 KB (9171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250420.0.338771` - unknown; unknown

```console
$ docker pull archlinux@sha256:759002d25c04d508019ead0b88bed58d624baf1398b2320942cc0963b265dfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11998045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0a0bd28354a804831d273e7a2205ccd835aac5247523fdd2ba9eb1e4d07358`

```dockerfile
```

-	Layers:
	-	`sha256:2238620d005e2863b7b1ec6f537e1d8b1b21d4356f617e4edf9451e4b2fa1abc`  
		Last Modified: Mon, 21 Apr 2025 22:34:50 GMT  
		Size: 12.0 MB (11986291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c41e7c38413c05affb373aa6b337ca9345e40825a802ec63a2976e48564c3df`  
		Last Modified: Mon, 21 Apr 2025 22:34:45 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
