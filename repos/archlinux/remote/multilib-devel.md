## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:c2c53d463f00eecf02ba3f3bb4035cf4fb01b0937329a9043b848eb8d5a73820
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:90cf52c153f13d76d3e9f0049cae9d5bbb0d19a9cc432d2dda15d9eed81a983b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341722455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b304069c628e718c14841fb8537473e9dc595abc3e3f85b592eb97a2620a8b5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f4207c155a5d4e78745234ffe4f665ad0c58299bde28ced8e73f91fefb05c2f7`  
		Last Modified: Mon, 13 Oct 2025 20:08:45 GMT  
		Size: 341.7 MB (341712195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d78f276a546ef06488eca8700198fd0f1051dc02511ecf5ec4e0ed903d8bb`  
		Last Modified: Mon, 13 Oct 2025 17:58:28 GMT  
		Size: 10.3 KB (10260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f6beada9dbed10e61f7f41ac38e9e7236eca1c44504f97db4af9636cde19e60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12399546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43065518a2fb97b4dbf8b62cd23ee1b3164d6f77d7c748bc83c585dec0204e06`

```dockerfile
```

-	Layers:
	-	`sha256:c9d16b54bbed4a9fef9d38691df582544e791c1f1d3a56f1614a3ab55c50e61e`  
		Last Modified: Mon, 13 Oct 2025 19:48:32 GMT  
		Size: 12.4 MB (12387735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01bd7d92fab6d6f458dbd52b87b59f5215048542ea41882846d84015a9741e5`  
		Last Modified: Mon, 13 Oct 2025 19:48:33 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
