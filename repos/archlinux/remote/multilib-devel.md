## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:730c6a9a02deccc529aab379d4e1862461be510a49fd54c3c809d4104fee66a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0ef15c9afbbce0bc61b86e0b1a1cccff48b886b2efeceb0992b25a0cd90d2365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331780513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a548c8d83b0af7a75c93f26629a75033fd47b085c8f3ef009b47a31e28550f72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.version=20250427.0.341977
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.created=2025-04-27T00:07:36+00:00
# Sun, 27 Apr 2025 00:07:36 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250427.0.341977' /etc/os-release # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
ENV LANG=C.UTF-8
# Sun, 27 Apr 2025 00:07:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f65bc684ebcc882fc0c3c6bac39fe5e12352323433e0ae4ed3b90823f539b59a`  
		Last Modified: Mon, 28 Apr 2025 17:56:42 GMT  
		Size: 331.8 MB (331770222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbaa5643ba2de775c37e9d80d9254a5ea7a6210ea9732fa9a94815b9620ea2b`  
		Last Modified: Mon, 28 Apr 2025 17:56:37 GMT  
		Size: 10.3 KB (10291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2d2d59ebf71513f07e01139c7ffef315bb04b0021d79761b8131c1dec50e8a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12266647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6ec447bd0b3a2795e3c64c8bf442f45692c62af68507c98ee8b58f656d29a5`

```dockerfile
```

-	Layers:
	-	`sha256:b73d154edcc2141fc7e388ad0f2b9c20c8a5acf38bc82fbd93c1c456c7029961`  
		Last Modified: Mon, 28 Apr 2025 17:56:38 GMT  
		Size: 12.3 MB (12254836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8030ff0221cd09c9dacafcefc35b1fd821ef8248128b681226ca453f3f82661`  
		Last Modified: Mon, 28 Apr 2025 17:56:38 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
