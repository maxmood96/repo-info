## `archlinux:multilib-devel-20260607.0.541780`

```console
$ docker pull archlinux@sha256:e6c4eacdc7d29cf643f18e4cfb7a31a2e893a58812fb848ba082f8998e7ea79d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260607.0.541780` - linux; amd64

```console
$ docker pull archlinux@sha256:bac38ab00bbb724ce28c462090a16c945b63a240decb6a7cf379bdbbcd965bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325614860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4432acb6ef1440624e07af21515fc71e8acf2c675d70b286b05a2057b5c36f2c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.version=20260607.0.541780
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.created=2026-06-07T00:09:31+00:00
# Mon, 08 Jun 2026 18:52:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jun 2026 18:53:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260607.0.541780' /etc/os-release # buildkit
# Mon, 08 Jun 2026 18:53:06 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jun 2026 18:53:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:33c542c269fab0fd2e79e751ea20038d1a2b9f0b429f58b9d3c2557c5198706a`  
		Last Modified: Mon, 08 Jun 2026 18:54:07 GMT  
		Size: 325.6 MB (325602302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c928c01f537d741e5384fb5a33143a6e0be2634345a1ddd8d1e3f71dd5bbd3f`  
		Last Modified: Mon, 08 Jun 2026 18:54:01 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260607.0.541780` - unknown; unknown

```console
$ docker pull archlinux@sha256:85beb6033726c2975b70e73ae357bad61a36871fb12466b42855b32b102f1a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14668220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8360cc6388d36e4dda0c02ede03d280e4c4a02d41f7e060cdb1cc7684f8a860d`

```dockerfile
```

-	Layers:
	-	`sha256:b5e77fc1adf1127c92c9b1546ef6c7135128f200100a85d4e0545a20d60c37a9`  
		Last Modified: Mon, 08 Jun 2026 18:54:02 GMT  
		Size: 14.7 MB (14656453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce182fab25d3f5e50b56f19ef7f7769a45867dcd1f3f9f23c7522e75fdf7ef15`  
		Last Modified: Mon, 08 Jun 2026 18:54:01 GMT  
		Size: 11.8 KB (11767 bytes)  
		MIME: application/vnd.in-toto+json
