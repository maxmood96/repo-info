## `archlinux:base`

```console
$ docker pull archlinux@sha256:dbcf6a01a24a56c96b179d40f2425fd257f58e6ff8c5c54c1aa66251442d6f80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a10e51dd0694d6c4142754e9d06cbce7baf91ace8031a30df37064d1091ab414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151275787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e34eb59b71012351582a045b4fff0f634e7419658a7110e2f83fe92a1c9c9a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.version=20240908.0.261281
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.created=2024-09-08T00:07:27+00:00
# Sun, 08 Sep 2024 00:07:27 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240908.0.261281' /etc/os-release # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 00:07:27 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:48c737288e6ef23c01fa5e142b7634c1350a21e5861dc935a45de8c004fb10ed`  
		Last Modified: Mon, 09 Sep 2024 19:04:38 GMT  
		Size: 151.3 MB (151267511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98025c0a629bee7f87f0a8a61dfa36c301f809d98d57997906d7e99b1b8a88`  
		Last Modified: Mon, 09 Sep 2024 19:04:34 GMT  
		Size: 8.3 KB (8276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:bd57c1bbb7e09e2ff312b49d6c4d6dde2fd55ab4077ca82c936dac32ed1084c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66e83baba40b005da4c04d9de63bbacb625fc60c71b9ce9fc9b6c35df1eeae6`

```dockerfile
```

-	Layers:
	-	`sha256:f60d3ae488e9d9793aa105257d6b52d31de4588a33c852c42f0d70b3f283aaf2`  
		Last Modified: Mon, 09 Sep 2024 19:04:35 GMT  
		Size: 8.1 MB (8103997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35492009cbb34845e893e537fb1729615d7daa4a5c1d0b3ef47b21796b85204`  
		Last Modified: Mon, 09 Sep 2024 19:04:34 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json
