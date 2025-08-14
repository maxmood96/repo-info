## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:92a0740113bd2af7f38bf7c9992efd5ee61e745e9934326eb50ecdf24495b055
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7bf5d00a7e8473652564baba1da92ca3ad2db6ad9855b0a3255aabe68411c778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307034893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952307d2bab25b4808157fe3ed835868bea8b5954145ffa666e39f61eb40e8ac`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250810.0.398652
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-08-10T00:07:35+00:00
# Sun, 10 Aug 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250810.0.398652' /etc/os-release # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 10 Aug 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:515896c7cc7d6fef4d3fbf34e346c6c9051e0be95d5d732aa229d9f351acf9fb`  
		Last Modified: Mon, 11 Aug 2025 19:50:19 GMT  
		Size: 307.0 MB (307025742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1db20b211cf7a03cc50031438ce24251d1ce629d977877be6c7141737dc4b92`  
		Last Modified: Mon, 11 Aug 2025 16:41:44 GMT  
		Size: 9.2 KB (9151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:5ee14bacfba5eaa81d8eabb78565830b81ab0d654ed403b9fe9934b50bd71b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b55c988109051f320608ad79249a3c615f470894eb60c3d37e36041586ca43`

```dockerfile
```

-	Layers:
	-	`sha256:0ebd39a228b0ed224fae0d9cd176039aaf0fb24f45d018747c60b0d231e5ec11`  
		Last Modified: Mon, 11 Aug 2025 19:48:21 GMT  
		Size: 12.1 MB (12063807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0339765509ae6229a50dbe98118fa7cfe5e72b53130521b9a8d8ef462a73313a`  
		Last Modified: Mon, 11 Aug 2025 19:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
