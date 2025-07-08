## `archlinux:base-devel-20250706.0.377547`

```console
$ docker pull archlinux@sha256:7beca11cc5203d0d7ee2e1202637f2600233b9e6195209f503d42ba356d414e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250706.0.377547` - linux; amd64

```console
$ docker pull archlinux@sha256:5c69359f124f1cf8a9893316275a365d3e385bedefb14b303b05dc32c756a62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (287989756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50566aeecbb8d701123cb31d46526e372d2cd8335c206a50a2344364b537349d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9f0d5de9ddb4d81aa2a08509561163ca7693879d92ac0b865ce0886de4c37f32`  
		Last Modified: Mon, 07 Jul 2025 22:53:36 GMT  
		Size: 288.0 MB (287980592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592358f41916bd8be2c671e8d2fa64d6177220b1c122ccd0a7ff526d0ba6f4b3`  
		Last Modified: Mon, 07 Jul 2025 20:42:39 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250706.0.377547` - unknown; unknown

```console
$ docker pull archlinux@sha256:592c70285fb2f9541e249d9b36fb83fdd6af648ddf902502ddf23bce643e823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12023256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cab1edfec4b64f88b3e28bf3619d1a440b7de9f7656c72e9d06b0894761aad`

```dockerfile
```

-	Layers:
	-	`sha256:486429721b9f31a7973dea12cfccc79d6002d6d1d82204e6192dc655ebe4bd9d`  
		Last Modified: Mon, 07 Jul 2025 22:48:20 GMT  
		Size: 12.0 MB (12011502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5bbdf1f466f6084825933d45522be922045282ab20746134f5a45922a972c0`  
		Last Modified: Mon, 07 Jul 2025 22:48:21 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
