## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b2769eb9f333a0af56944cf6aeccaa59011c1a0516ef49ebb4f409e6df9215a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f795a0b7bcae2aed78ff75c160e432f29f5022318ed775c9ebe7239c6e980e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272433307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb3c70ba41ba6d5e07cac213fe57b5469ba2763f3ea33a57f635f0e7b65a127`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f216b571f44a239d4f4c6d69a1dda566c45a9a44e799822dafdc9b32f5d6668`  
		Last Modified: Mon, 11 Nov 2024 18:58:44 GMT  
		Size: 272.4 MB (272424247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe5621576a3df3ebb05652537b68049fb9e3f436e27e360164a66aa89b43e7`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 9.1 KB (9060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d1feb1e3b4b3eaf4ad5b1b9c2baebca7a76f6113f9a0c0ee74d8de63f1caec1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969240571d7bd07eb46191fb9a61d4f9079b5101ede5e258f939e9c403c478d0`

```dockerfile
```

-	Layers:
	-	`sha256:274f4ca6bd6fba43e6f82acb2a725d3182c8de0f487cfbc1f1612179524c4598`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 11.9 MB (11895685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f1c4d2ba147e6ed43b078f92e41fb934c58b58168f43baf1af72ed6fd07c65`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
