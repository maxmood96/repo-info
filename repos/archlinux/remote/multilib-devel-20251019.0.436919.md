## `archlinux:multilib-devel-20251019.0.436919`

```console
$ docker pull archlinux@sha256:c52936673f184d8c3bdcebd4fc6d5403514bc18e175d26fa7c3793b72cbb1d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251019.0.436919` - linux; amd64

```console
$ docker pull archlinux@sha256:44e30138991d38036d0894982230cd74588aa5569e568493c85c1ab7d434d8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341725875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f53020a3b2fce039f6cbadb7aec91cb6c9c83ca993c5d126a5b5f643094addb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.version=20251019.0.436919
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.created=2025-10-19T00:07:20+00:00
# Sun, 19 Oct 2025 00:07:20 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251019.0.436919' /etc/os-release # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
ENV LANG=C.UTF-8
# Sun, 19 Oct 2025 00:07:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a43e711e3fbd4e30e7a99e9ce907fb06f984d509678fa60f3ca9fc42598baa7f`  
		Last Modified: Mon, 20 Oct 2025 22:56:53 GMT  
		Size: 341.7 MB (341715623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf121b786352eeee330d472642e8989ff20bceafcadb1623704f11275a118a0`  
		Last Modified: Mon, 20 Oct 2025 20:27:50 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251019.0.436919` - unknown; unknown

```console
$ docker pull archlinux@sha256:a295df9d8b1b9b58bcdd6f54e79f6212fd3412dacac22e41a5e7dbdd60d25b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12399580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934cf46797d3d466de5f1403ff14c1c4cc600d260c5f93bf68d55277e47e17da`

```dockerfile
```

-	Layers:
	-	`sha256:258189b3f3b436f10e31bf58372d8fb45c6a4c8d1cd6289d15e335dd2129aa5e`  
		Last Modified: Mon, 20 Oct 2025 22:48:29 GMT  
		Size: 12.4 MB (12387769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3430635cf28312485efb75431807ca09f28f462ecd8eabec6624433bdba2d19e`  
		Last Modified: Mon, 20 Oct 2025 22:48:30 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
