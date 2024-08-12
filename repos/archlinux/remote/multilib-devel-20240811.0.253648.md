## `archlinux:multilib-devel-20240811.0.253648`

```console
$ docker pull archlinux@sha256:5aa722de8945fa66550498935a47cd82eb500d1b77c7e93e9d27109704923eb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240811.0.253648` - linux; amd64

```console
$ docker pull archlinux@sha256:43406cf54cac37988bce93ad3da51193b7d5aed9b770d1f5a514759983e52dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321618527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d75688e4843e6be26eac02cbbb379da2ba1fbfc8056b25365207c23bdd0083`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20240811.0.253648
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-08-11T00:07:52+00:00
# Sun, 11 Aug 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240811.0.253648' /etc/os-release # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 11 Aug 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f58303c2dafef45f1aae7aeb62afc703cee59842d9290051b70b6b85bff175da`  
		Last Modified: Mon, 12 Aug 2024 16:57:17 GMT  
		Size: 321.6 MB (321608337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f69d045dd51ec19952ad9dd37480cf3e58afee258a413c342a51a0d959b7f`  
		Last Modified: Mon, 12 Aug 2024 16:57:12 GMT  
		Size: 10.2 KB (10190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240811.0.253648` - unknown; unknown

```console
$ docker pull archlinux@sha256:3c4f44b741b296170f8cc4c3f1177b007ec0c297d27971afa5e7b130e9a805fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d8ee0b964342b4be44f4dfa7083540490819118326f03a915a7342e974caf7`

```dockerfile
```

-	Layers:
	-	`sha256:4694a60ac3904dbc05e3dcc03ef09ebbc4b80273f1d57236577ff4772ce2f480`  
		Last Modified: Mon, 12 Aug 2024 16:57:13 GMT  
		Size: 12.1 MB (12085504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b59507ebfb5d379421cd9016fc2a44d7c95960df53a00a31b5e7e19f850916bf`  
		Last Modified: Mon, 12 Aug 2024 16:57:12 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
