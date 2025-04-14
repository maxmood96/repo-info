## `archlinux:multilib-devel-20250413.0.335299`

```console
$ docker pull archlinux@sha256:521ba353716efe7a8938ef4cebd8eec63b3112d0d42f927ef7a095de71361aab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250413.0.335299` - linux; amd64

```console
$ docker pull archlinux@sha256:5877e4f34b73dde77086bdb7b8c2cdc2ac909cac0ccc7234b3e1e42537f4d736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331766952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c7309fde5a9ee0b0b41a84bd8546da9b425608be3a69f9f9a73a135f1b7e4c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.version=20250413.0.335299
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.created=2025-04-13T00:07:50+00:00
# Sun, 13 Apr 2025 00:07:50 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250413.0.335299' /etc/os-release # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
ENV LANG=C.UTF-8
# Sun, 13 Apr 2025 00:07:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7c59532cd91bd88ed8d5a515903378df2df6ec04b43146fbf79d48c0b357d9b1`  
		Last Modified: Mon, 14 Apr 2025 18:01:34 GMT  
		Size: 331.8 MB (331756653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6691d2c981d2211a8e6a6d4a18c2793d3e28738e708a72d402f0963b3316d4`  
		Last Modified: Mon, 14 Apr 2025 18:01:28 GMT  
		Size: 10.3 KB (10299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250413.0.335299` - unknown; unknown

```console
$ docker pull archlinux@sha256:3e5012423e5b160b9ec5833767d6c9ece50e09cc6207f141591ca63efe78fdb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12265410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a10eb9944685c52afdcc0e99b0a2279b283203bb3a481a66e1c787ab1e3b1e`

```dockerfile
```

-	Layers:
	-	`sha256:420d8c5d9735ac9dd061250c023cebcf3ee6d76290b91fe03bc92dbba04a9d03`  
		Last Modified: Mon, 14 Apr 2025 18:01:28 GMT  
		Size: 12.3 MB (12253599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b6808055b6a2ee364b1bc9cc1690b76de484fdba7c95dab14b1a67dbaf9db8`  
		Last Modified: Mon, 14 Apr 2025 18:01:28 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
