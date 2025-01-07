## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:83c6137d571e9c200fe12425cfb8f568d2b07c4bfebcf54a85752cbdab5db402
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:1fdc20a8cc97aa4e33705ee9458e97d0768a53a19fe4658f88b8ed0fda084dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323773511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0516e649224737387e5d54cd8d688daf2f295843abad8d22704fd8dd9b8157f8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241229.0.293060
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-12-29T00:07:35+00:00
# Sun, 29 Dec 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241229.0.293060' /etc/os-release # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 29 Dec 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f5328e0670e08fe414577918346f76fcb4d4f11d79607ca4de12c8ccf9a794af`  
		Last Modified: Thu, 02 Jan 2025 19:29:48 GMT  
		Size: 323.8 MB (323763288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d512af53f6bdab09a1a17db17f768ac11a2af7c63058ff13a474dcb9b5f1d4b`  
		Last Modified: Thu, 02 Jan 2025 19:29:43 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:ec4a71aa2d6be867da722570d0c04aa0ec293ce666a1f3b15e2620d9474f9cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa3fe87abbc1c01628b94fa5ccc88653228a2f151860029c2fa0ea470568cff`

```dockerfile
```

-	Layers:
	-	`sha256:69e57fae915251e1ac5985cee8a0673b0f1bdd96e56db5cbf122ae12e4d95ad4`  
		Last Modified: Thu, 02 Jan 2025 19:29:43 GMT  
		Size: 12.2 MB (12153736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc4a5129e1bc10603215924119a907c069c8a01c8bb976b73765d7db9e8727de`  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
