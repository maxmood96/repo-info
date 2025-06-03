## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:3f7f6e4ddc04d4f6a8cb36b4af9e2290371f36dde1650c5177b50b7233706a35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6e2243eb90d12e09cbddf7d5297ac44195928282881562e6c9d339b44c029fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287135856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2d27cb2ad3b2f7d3491dd4607dd0472e8da9c34bf2fc74a5877bb7ef49bd20`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250601.0.358000
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-06-01T00:08:08+00:00
# Sun, 01 Jun 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250601.0.358000' /etc/os-release # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 01 Jun 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9eba33a123ffc0a67ad7c9fc71d74e5256149041186372c705e8ad4ca87f9ef2`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 287.1 MB (287126647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a033bf9719d0e801b428a756787b040ecc18dd0d1c1cfdda275e839bf1a2cd7`  
		Last Modified: Tue, 03 Jun 2025 13:32:29 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:58eb529e583d6583df0e8260bda56b2d8ad28c39f3463049fad7a566793cac67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12041897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b2fdf1a33d27824c978e00195d6382520bf710a70dc59c30e0f138bec9058d`

```dockerfile
```

-	Layers:
	-	`sha256:a653be72637f899fa9eedc6023ed722fe12ae3a14e14346ad22918102ece5738`  
		Last Modified: Mon, 02 Jun 2025 16:52:42 GMT  
		Size: 12.0 MB (12030143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1edbe1f07b5d13c5b76883241fc3c8eef54b37fb5c272566e8614ae3fca9850`  
		Last Modified: Mon, 02 Jun 2025 16:52:42 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
