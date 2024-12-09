## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:ad7265dcfc77e1de728808f70b38af05f2e15af9d49e2bda7eb78c33c4af9f8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f2d673da953a7eafb0d6d0aaf0696ba6504b316cb6c266d2d1e6e1ec76a11ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273417914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc662799b750cee2550eb81a5cb5b892640c0e5ded2b4711a8519463b68fdbf3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.version=20241208.0.286830
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.created=2024-12-08T00:07:49+00:00
# Sun, 08 Dec 2024 00:07:49 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241208.0.286830' /etc/os-release # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
ENV LANG=C.UTF-8
# Sun, 08 Dec 2024 00:07:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4dddf33f2d22fe711bc3b375cc5bf972dcb73a808ac73e9580261bd89629b88e`  
		Last Modified: Mon, 09 Dec 2024 19:29:05 GMT  
		Size: 273.4 MB (273408836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6e8053ae34cf074b762d4d6648fca119c3913903624dd72675af890497a4a5`  
		Last Modified: Mon, 09 Dec 2024 19:29:01 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:56658971362ac1af8bd4787b6df9adec16854da79d419b9a1a9eb99fe159da10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9ed79f6e4e53dd39251af10cb392667c41c3760638c3c72c968fbc340b60e4`

```dockerfile
```

-	Layers:
	-	`sha256:a9892998169112e5dbc0db679e82e8c8ab5f304476aea015725973a0bff023f4`  
		Last Modified: Mon, 09 Dec 2024 19:29:01 GMT  
		Size: 11.9 MB (11896942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79615ce59fc128734ad8beb6b434c4f76d10ffb033d7d7d2f464ddd83f0b43ee`  
		Last Modified: Mon, 09 Dec 2024 19:29:01 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
