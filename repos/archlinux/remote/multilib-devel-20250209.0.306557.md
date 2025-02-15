## `archlinux:multilib-devel-20250209.0.306557`

```console
$ docker pull archlinux@sha256:bdb4a8d2bb14339e2c8d782da829b411f2bf04f328c521730f765291799195d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250209.0.306557` - linux; amd64

```console
$ docker pull archlinux@sha256:8ff14dbb10ae1f83d829a38e17b67418a08924876e686add1da9bb14f749aaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51df7133cb3743c40ebd4defe13a570da07fbfa0fc243ca6fd2235fcb0868af`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:61c8fceafc7f0cdee9f810aaad8a75bd636d2b072b8452854e73c7c6f001b2c0`  
		Last Modified: Mon, 10 Feb 2025 21:05:30 GMT  
		Size: 328.8 MB (328805658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a65587c9714ca6ad5a8e17b56eafc9d96e8f8dc887fd8dd8bdaff6458093e02`  
		Last Modified: Sat, 15 Feb 2025 00:06:34 GMT  
		Size: 10.2 KB (10219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250209.0.306557` - unknown; unknown

```console
$ docker pull archlinux@sha256:6d844b9620d501968ea96f0e065f8414a6081ce89b35694587139121b1843266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7e95d548c3ee53012b53084e22590c7c706efe4e92c82adc088d3cf5e6a53f`

```dockerfile
```

-	Layers:
	-	`sha256:38747e51b379c4bf7f793ca3cf267721bf9dd50f7749e8313eb31e8d2390d655`  
		Last Modified: Fri, 14 Feb 2025 23:48:23 GMT  
		Size: 12.2 MB (12165053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20d15760832cc19f95649693a569c324d37db3c647121e7791593ebac964f17`  
		Last Modified: Fri, 14 Feb 2025 23:48:23 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
