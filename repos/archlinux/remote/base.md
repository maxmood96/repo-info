## `archlinux:base`

```console
$ docker pull archlinux@sha256:65b8373574abc1afda6c77ca01bba81ba02cb3779ced8ae1b5cd29f48d75c4f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c9b9e00238d67eb25868d59c658b0566d49df3d0d5e6cfdc88a8099d966dfadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151211271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0783ec4488140fe48524781040a1528f957e86bd29f08e7fac97c155afdef7d6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a177a8b9b0eb48ecc5621b8999f2a3ffb3b838af7149516ae728e3de3d265c95`  
		Last Modified: Mon, 28 Oct 2024 17:57:21 GMT  
		Size: 151.2 MB (151202982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a98e2032b813b85b356987b3e9942c397d04b3452d988da53048eeaa9ef3ac3`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 8.3 KB (8289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:b5ac2147e2399d71365a4e21c3c04d34ff173a61be6b4756753b5b2ff52b429c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dad605717143b6aa0b156ac2b8dd89c837af0aa477b8f57bfa5dd9d2f4c6cf4`

```dockerfile
```

-	Layers:
	-	`sha256:c501b60485132b041b536e0c71104a796f62edb28dcdd20446461663d50fb590`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 8.1 MB (8144185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d231dd67e2a4baa5f9582e3adacde08c6f019ea6c1221160eec75e5304154f`  
		Last Modified: Mon, 28 Oct 2024 17:57:19 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json
