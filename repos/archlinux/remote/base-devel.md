## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:2003c2bad5c08a96eb6cfec8b82322868c15378a2c91d9e4cbe3918372101c88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3e693497e5a4a3a0075c9c2fed4dc8bc2b85b869428bad32fc6aab9d9a3b283c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280766642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee3009458243b371059558e3a5924562e8aab316ddd354c5ec4bcbd0c05f6eb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.version=20250323.0.325468
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.created=2025-03-23T00:07:47+00:00
# Sun, 23 Mar 2025 00:07:47 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Mar 2025 00:07:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250323.0.325468' /etc/os-release # buildkit
# Sun, 23 Mar 2025 00:07:47 GMT
ENV LANG=C.UTF-8
# Sun, 23 Mar 2025 00:07:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:893d35ab08423a4333663b24e409ce16378afb62b4bbc0b525cf4e768e6344c3`  
		Last Modified: Mon, 24 Mar 2025 17:03:22 GMT  
		Size: 280.8 MB (280757591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae6585339a90f6b782690794886b2a8fce5d810407f20181bb4a4209db780a`  
		Last Modified: Mon, 24 Mar 2025 17:03:18 GMT  
		Size: 9.1 KB (9051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:b3117fbf42b83603a0ee9c8a5bb49aff7eb1eae1bdf4d1ed7e429e321f5dd410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11991419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216ab56a52f4e05890f92f648ad63993ef7e0db8e98d1bbc873306307089917f`

```dockerfile
```

-	Layers:
	-	`sha256:5f68d25f792e742642c4c5cae880259db66a558cac8b42c1bdc81e5feba42aa6`  
		Last Modified: Mon, 24 Mar 2025 17:03:18 GMT  
		Size: 12.0 MB (11979665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8da1b296b55634382afc7fa84f02a18aa50c7eeb19b9390f2dab7b8eae2d6c`  
		Last Modified: Mon, 24 Mar 2025 17:03:18 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
