## `archlinux:base-devel-20260524.0.535079`

```console
$ docker pull archlinux@sha256:25074821d28e54a0bbbd87a88d392f1489be9bd815ee5c60744be6e57fd500d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260524.0.535079` - linux; amd64

```console
$ docker pull archlinux@sha256:6d08b7067286234b755a28340b6bd89f3a2289233dbca3c361464f27ecae8f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303791039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580435224cc79643afa10d15c96e18bcd2e5b2f6bed0f6d9ca0cec3088c0561b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.version=20260524.0.535079
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Tue, 26 May 2026 18:59:47 GMT
LABEL org.opencontainers.image.created=2026-05-24T00:12:57+00:00
# Tue, 26 May 2026 18:59:47 GMT
COPY /rootfs/ / # buildkit
# Tue, 26 May 2026 18:59:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260524.0.535079' /etc/os-release # buildkit
# Tue, 26 May 2026 18:59:54 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 18:59:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0918ff50f07eb1e93987401d7008971f93c893f4a592c183723f4618bcdb15cf`  
		Last Modified: Tue, 26 May 2026 19:00:51 GMT  
		Size: 303.8 MB (303779612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becec186e69bb6eaf326716f41694848554950a23f6583c61fcf4d37f35558d8`  
		Last Modified: Tue, 26 May 2026 19:00:43 GMT  
		Size: 11.4 KB (11427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260524.0.535079` - unknown; unknown

```console
$ docker pull archlinux@sha256:2114986abe1f78c7f73934aa10e4bcfdaf7abda58883c9cd9f8cbbf8b0aa38bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14396300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67dd7c236d3cc3a189f9b37e032ccd58fc18b49153d53bfed8b20e21436b1dcb`

```dockerfile
```

-	Layers:
	-	`sha256:4b5809322b6a47d72ba0c1c44175d0462f0a744516e79c2a700033e39e941958`  
		Last Modified: Tue, 26 May 2026 19:00:46 GMT  
		Size: 14.4 MB (14384588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670480bc2b7f09b900dadacf69e0d3601e43f9088510995516a0f58d4023721c`  
		Last Modified: Tue, 26 May 2026 19:00:43 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json
