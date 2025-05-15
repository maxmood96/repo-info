## `archlinux:multilib-devel-20250511.0.348143`

```console
$ docker pull archlinux@sha256:8852c489e3b0daf5d8afe1c94b4a4dd8de38176060a5971da3a2776e62609caf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250511.0.348143` - linux; amd64

```console
$ docker pull archlinux@sha256:ff718773c826ed5de0b9ec276971255531eaafe903772144c905ec0928aa0ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338205246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0737f8c336251e31c3f954aa4276ac32957996ba981aa300aa816316b45f843e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250511.0.348143
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 11 May 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-05-11T00:07:38+00:00
# Sun, 11 May 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 May 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250511.0.348143' /etc/os-release # buildkit
# Sun, 11 May 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 11 May 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f6d25a390ff1e44723dbbc555061dde908cb77ebce6778723e4ce827eaa6132b`  
		Last Modified: Thu, 15 May 2025 20:17:24 GMT  
		Size: 338.2 MB (338194960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56fade2eeed012139f19a60b32ed1b404bb12638044328c99efb8081ffe0d94`  
		Last Modified: Thu, 15 May 2025 20:17:11 GMT  
		Size: 10.3 KB (10286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250511.0.348143` - unknown; unknown

```console
$ docker pull archlinux@sha256:107e8c8821204655b83d8d6cb710a3786868340eb3f2883d1d62e97c6fb125c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12306665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2683507c077fa976fd740e41e31a3b97cda0b7e17cfa1696ba23281bfb92cc7`

```dockerfile
```

-	Layers:
	-	`sha256:8257bc2a4074a74246e47fd6cfde70c992860d0cac6e619ef012b660dadf90f6`  
		Last Modified: Mon, 12 May 2025 19:09:44 GMT  
		Size: 12.3 MB (12294854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd54c138d71de884b46a37934c00bae1b37beefdfd1ef708f047716dab652dc`  
		Last Modified: Mon, 12 May 2025 19:09:44 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
