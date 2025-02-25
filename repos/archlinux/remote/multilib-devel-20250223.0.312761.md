## `archlinux:multilib-devel-20250223.0.312761`

```console
$ docker pull archlinux@sha256:d5e028f1638d310cc7a9fb11e1b0ea405d6b1c9c62c3757f7981ab08c4e91cc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250223.0.312761` - linux; amd64

```console
$ docker pull archlinux@sha256:6eb24c1061ccb1c6e41a737cf524aac5f47076531a3db7d98cb89c767009bb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330257679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769e3859181049fccd96195146a835445896cd4616647494d8779a888e0638e1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
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
	-	`sha256:30697cacdae779eb2353295674328b41e46159d06e3b92f3984b2d6e608e1b27`  
		Last Modified: Mon, 24 Feb 2025 20:29:50 GMT  
		Size: 330.2 MB (330247473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5d62fb6565a7832cac1862cefbc4b3649084e20aab1ec2125ae083d5e03b0`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250223.0.312761` - unknown; unknown

```console
$ docker pull archlinux@sha256:252c57a7807566d185df378c2e28a75ff506dec712d916698a4524451ce14676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12248718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0217ab4d0e2bba7c6ef486029aa76cac1221cc5d46696915b0cde7efc659a4ce`

```dockerfile
```

-	Layers:
	-	`sha256:729ca1f9fbf7be78a15a301d453ac2f26e5095edefa498ea172effc0c29c92c6`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 12.2 MB (12236907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20bd475c5d21685ba45825c8cd2367a748391d8fb703bf93f66cc8a1df8fcbae`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
