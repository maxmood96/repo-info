## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:6d743681334a9a3859a1b2633508e2396425085cda41639b1ef35fa74618f9b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:640853c4edb541414067534ad93a86ede65694ffbad88a0dd8cbe3a6eb52491f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271541006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31fe7924ac8c0839a4d426172c2493b6cdf148bfd1c0b519b5bd68923ad7cd64`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20240714.0.246936
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-07-14T00:07:41+00:00
# Sun, 14 Jul 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240714.0.246936' /etc/os-release # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 14 Jul 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c5e7e9ca8c90472562dcd8bbf294446d70a3e2e9a90b7dcffa68a2e4bcc1b0bd`  
		Last Modified: Mon, 15 Jul 2024 19:56:02 GMT  
		Size: 271.5 MB (271531942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c906eceebd38638816e79140e33329ce7fb74b03e0c028433816abcca811829`  
		Last Modified: Mon, 15 Jul 2024 19:55:55 GMT  
		Size: 9.1 KB (9064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:ee56500c52b86e0b9e759bb4a33685197ddd06044760714d875180a749750278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11798888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438ff722dc504d9ccd192b0ca4c4032948dbd34a91877ef90ae7671e8dfc3444`

```dockerfile
```

-	Layers:
	-	`sha256:f386c6d13b5e60d0f8690dd1cb5346cf3681d471f3bbfc137db46f91243ddf6c`  
		Last Modified: Mon, 15 Jul 2024 19:55:56 GMT  
		Size: 11.8 MB (11787385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df627cede0dee729d485e2b522d0f40988f4fbdda91fdedb11616e25775dd2e`  
		Last Modified: Mon, 15 Jul 2024 19:55:55 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
