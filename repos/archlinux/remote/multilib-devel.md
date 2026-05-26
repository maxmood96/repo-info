## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:55a7352e9b556656a0eed60bb72f4a546b5d06aec060fb295d7e98dc02c98feb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0f699314eda17eb77f2026c693c35fcba214b984ce0564fe4e9440d86d8d7f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.2 MB (326164515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce52ca4c5ef44376d55a03d96a991b4d9b3a0d2be2d8a6d78806620b43a1d48`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.version=20260524.0.535079
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Tue, 26 May 2026 19:00:10 GMT
LABEL org.opencontainers.image.created=2026-05-24T00:12:57+00:00
# Tue, 26 May 2026 19:00:10 GMT
COPY /rootfs/ / # buildkit
# Tue, 26 May 2026 19:00:18 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260524.0.535079' /etc/os-release # buildkit
# Tue, 26 May 2026 19:00:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:00:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3f752e590d610a34618f941771d6c6bcb73c7309514378d23abd9e46b4d49764`  
		Last Modified: Tue, 26 May 2026 19:01:14 GMT  
		Size: 326.2 MB (326151948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac52b4c2ab0b6fc7dae672d718111b3a451ac4c49dbf674d9df2c9f0ef962fe`  
		Last Modified: Tue, 26 May 2026 19:01:07 GMT  
		Size: 12.6 KB (12567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:cd2cb65e3ac46f802b0feb77b7a0361074878ffa6cfa113d241a8753d23eaac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14667097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa6525b6a729e8ee43315ee7515522b0e83b2c3305c08022f602e7e311ce799`

```dockerfile
```

-	Layers:
	-	`sha256:cf7c77ac1888f825e7cbfba64f28b61719fb1548c5857f8970d2663dab501035`  
		Last Modified: Tue, 26 May 2026 19:01:08 GMT  
		Size: 14.7 MB (14655329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31c79f7d6fa78665fce270ef22f1a6008035eaaa6479d22b6def9cf1b05b72`  
		Last Modified: Tue, 26 May 2026 19:01:07 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
