## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:6ec1f5073a94d877ae97ebf68e507f709b395c7a90005fe92d9db1c21f933077
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:80ee11bda3cb40c46061bbc91db00e3eb8e6147cb17189b4dc9554e501c791a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254000910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed09359b140a8876e61214bec59f1cde93757b75162d07afdb5c04e9d01cab3f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.version=20260510.0.525573
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.created=2026-05-10T00:08:50+00:00
# Mon, 11 May 2026 20:57:44 GMT
COPY /rootfs/ / # buildkit
# Mon, 11 May 2026 20:57:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260510.0.525573' /etc/os-release &&     true # buildkit
# Mon, 11 May 2026 20:57:49 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 20:57:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:45e67d8175df84610a18968cd899c0f1ca5acf749b8fc9a24dc8f7035e56010b`  
		Last Modified: Mon, 11 May 2026 20:58:35 GMT  
		Size: 254.0 MB (253991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376abe05a3122ee96f2b50c9d6adf26e4ed30b70f3aecf3f320590b853e67f9d`  
		Last Modified: Mon, 11 May 2026 20:58:29 GMT  
		Size: 9.2 KB (9168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:73a825d32cfe541e3c112bdd851f6968e5ef241b4e88f3d8ef3e7015ca9e5f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12048111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f1dfba0a6be5e8b752412b7682e85c615e71f08430b816c2697e4dca2c81fb`

```dockerfile
```

-	Layers:
	-	`sha256:ac3b99348eff9b35f9d117d7df1d35ae987c7d7b30a37b113788be2e3016cc22`  
		Last Modified: Mon, 11 May 2026 20:58:29 GMT  
		Size: 12.0 MB (12036322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08208c9270af4154939b3ffc42299b11b25c25113bb61ab7d9aabbdf36018946`  
		Last Modified: Mon, 11 May 2026 20:58:29 GMT  
		Size: 11.8 KB (11789 bytes)  
		MIME: application/vnd.in-toto+json
